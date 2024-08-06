install.packages("ggplot2")
install.packages("leaflet")
install.packages("shiny")

# importation des packages
library('ggplot2')
library('leaflet')
library('shiny')

# Charger les données
data <- read.csv("https://raw.githubusercontent.com/Eulalie95/myrepo/main/garderies_benin.csv", 
                 sep = ",", 
                 quote = "\"", 
                 fill = TRUE, 
                 comment.char = "")

# Afficher les noms des colonnes du dataframe
colnames(data)

colnames(data) <- c("name", "quartiers", "coordonnees", "indication", "latitude", "longitude")



# Visualisation initiale avec ggplot2
library(ggplot2)
ggplot(data, aes(x = longitude, y = latitude)) +
  geom_point() +
  theme_minimal()

# Carte interactive avec leaflet
library(leaflet)
leaflet(data) %>%
  addTiles() %>%
  addMarkers(~longitude, ~latitude, popup = ~name)



