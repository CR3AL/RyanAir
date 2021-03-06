# Ryanair Round Flights

Search for (round) flights, using: multiple arrival/departure airports, date range and day of week as input.

_I am in no way affiliated with Ryanair, use of this code for commercial purposes could be prohibited._ 

## Getting Started

Install using pip:

pip install ryanair

## Prerequisite 
Config.yml is required in the root directory of the script. A sample is included in the example folder.


### Example

After installing the ryanair pip package, you can proceed as stated below:
```
from ryanair import Ryanair,departuredates, returndates

ryanair = Ryanair()
```
Find departure flights. The function returns a dictionary and writes to excel.
```
departureflights = ryanair.flights(departuredates,outputfile='Departure.xlsx')
```
Find return flights. This inverses the departure/arrival airports.
```
returnflights = ryanair.flights(returndates,outputfile='Return.xlsx',returnflight= True)
```
Find round flights, based on the previous output
```
roundflights = ryanair.roundflights(departureflights,returnflights,outputfile = 'Round.xlsx')
```
## Contributing

Feel free to contribute to the project, in case of any questions please contact Crealcode@gmail.com

## Acknowledgments

* This was inspired by andre19rodrigues/RyanairRangeMultipleCheapest's repo 
