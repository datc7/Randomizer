# Description 

REST endpoint designed with the functionality of returning randomly generated numbers to the user. The endpoint allows for 2 methods of generation:

    1. Parabola - Gives a list of numbers with a higher ratio to the middle point
    2. Traditional - Returns a list of completely random numbers



### List of endpoints:

##### /distributions/randoms

|Method|Result|
|----------------------|----------------------|
|GET   |Return list of randomly generated numbers|
|PUT   |Update default generator|

__GET__

Returns a json list of numbers which are randomly generated using the normal distribution. 
Call can be made using the following:

http://127.0.0.1/rest/distributions/randoms


###### Parameters

| Parameter | Required                 | Result                                                                 |
|-----------|--------------------------|------------------------------------------------------------------------|
| start      | yes                       | Starting point |
| end      | yes | Ending point      |
| offset    | no                       | Used to page through results                                           |
| limit     | yes                      | The amount of randomly generated number your wish to receive           |





__PUT__

Allows you to update the deafult generator when using the endpoint. 
Call can be made using the following:

http://127.0.0.1/rest/distributions/randoms

{
    "generator": "-batch-"       // new generator
}

###### Generators

1. -batch- = Return multiple random numbers
2. -single- = Return single random number (Default)

##### /distributions/parabolas

|Method|Result|
|----------------------|----------------------|
|GET   |Return list of prabola generated numbers|
|PUT   |Update default generator|



__GET__

Returns a json list of numbers which are randomly generated using the normal distribution. 
Call can be made using the following:

http://127.0.0.1/rest/distributions/parabolas


###### Parameters

| Parameter | Required                 | Result                                                                 |
|-----------|--------------------------|------------------------------------------------------------------------|
| offset    | no                       | Used to page through results                                           |
| limit     | yes                      | The amount of randomly generated number your wish to receive           |
| start     | yes                      | Starting range           |
| end     | yes                      | Ending range          |
| middle     | no                      | Middle point         |




__PUT__

Allows you to update the deafult generator when using the endpoint. 
Call can be made using the following:

http://127.0.0.1/rest/distributions/parabolas

{
    "generator": "-batch-"       // new generator
}


__generators__
1. -batch- = Return multiple random numbers
2. -single- = Return single random number (Default)
