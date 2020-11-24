# Project Five, Part One: Acquiring, Modifying and Describing the Data: Team Challenge Question

## Team Challenge Question
The code block below shows my R script for project 5. I could not perform the extract command. The `ggplot` portion that is commented out would have yielded two combined histogram with density plots. The first would have shown correlation with population, the second with ntl. 


``` R
rm(list=ls(all=TRUE))

# install.packages("raster", dependencies = TRUE)
# install.packages("sf", dependencies = TRUE)
# install.packages("tidyverse", dependencies = TRUE)
# install.packages("doParallel", dependencies = TRUE)
# install.packages("snow", dependencies = TRUE)

library(sf)
library(raster)
library(tidyverse)
library(doParallel)
library(snow)

setwd("~/Documents/fall2020/DATA100/r_folder/project5")

### Import Administrative Boundaries ###

load("tun_adm1_2020.RData")
load("tun_adm2_2020.RData")


setwd("~/Documents/fall2020/DATA100/r_folder/project5/lulc")

f <- list.files(pattern="tun_esaccilc_dst", recursive=TRUE)

lulc <- stack(lapply(f, function(i) raster(i, band=1)))
nms <- sub("_100m_2015.tif", "", sub("tun_esaccilc_", "", f))
names(lulc) <- nms

topo <- raster("tun_srtm_topo_100m.tif")
slope <- raster("tun_srtm_slope_100m.tif")
ntl <- raster("tun_viirs_100m_2015.tif")
lulc <- addLayer(lulc, topo, slope, ntl)
names(lulc)[c(1,10:12)] <- c("water","topo","slope", "ntl")

# plot(lulc[[12]])
# 
# plot(lulc[[8]])
# plot(st_geometry(tun_adm1), add = TRUE)
# 
# plot(lulc[[10]])
# contour(lulc[[10]], add = TRUE)

ncores <- detectCores() - 1
beginCluster(ncores)
lulc_vals_adm2 <- raster::extract(lulc, tun_adm2, df = TRUE)
endCluster()
save(lulc_vals_adm2, file = "lulc_vals_adm2.RData")

# load("lulc_vals_adm2.RData")
# 
# lulc_ttls_adm2 <- lulc_vals_adm2 %>%
#   group_by(ID) %>%
#   summarize_all(sum, na.rm = TRUE)
# 
# tun_adm2 <- bind_cols(tun_adm2, lulc_ttls_adm2)
# 
# ggplot(tun_adm2, aes(pop20)) +
#   geom_histogram()
# 
# ggplot(tun_adm2, aes(log(pop20))) +
#   geom_histogram()
# 
# ggplot(tun_adm2, aes(pop20)) +
#   geom_density()
# 
# ggplot(tun_adm2, aes(log(pop20))) +
#   geom_density()
# 
# ggplot(tun_adm2, aes(pop20)) +
#   geom_histogram(aes(y = ..density..), color = "black", fill = "white") + 
#   geom_density(alpha = 0.2, fill = "#FF6666") + 
#   theme_minimal()
# 
# ggplot(tun_adm2, aes(topo)) +
#   geom_histogram(aes(y = ..density..), color = "black", fill = "white") + 
#   geom_density(alpha = 0.2, fill = "#FF6666") + 
#   theme_minimal() 
```
