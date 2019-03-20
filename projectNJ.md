

require(shiny)
require(tidyverse)
require("shinyjs")

list_choices <-  unique(msleep$vore)[!is.na(unique(msleep$vore))]
names(list_choices) <- paste(unique(msleep$vore)[!is.na(unique(msleep$vore))],"vore",sep="")

ui=navbarPage("NBA features",
              tabPanel("First Page",
                       fluidPage( 
                         sidebarLayout(
                           sidebarPanel("Side Bar panel"),
                           mainPanel("Main panel, Output")
                         )
                       )
              ),
              tabPanel("Second Page",
                       fluidPage( 
                         sidebarLayout(
                           sidebarPanel("Side Bar panel"),
                           mainPanel("Main panel, Output")
                         )
                       )
              )
)


server <- function(input, output, session) {
  
}


# Run the application 
shinyApp(ui = ui, server = server)