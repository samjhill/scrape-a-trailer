# Car Guru

Collects current auction information from Bring-a-Trailer and analyzes it using OpenAI to identify if a car is a good deal. It also raises important items to look out for.

## Sample Response


Listing: 20k-Mile 1994 Mazda MX-5 Miata M-Edition 5-Speed

https://bringatrailer.com/listing/1994-mazda-mx-5-miata-m-edition-6/

I would advise that the 1994 Mazda MX-5 Miata M-Edition in Montego Blue Mica over tan leather upholstery is indeed a worthwhile deal considering its low mileage and excellent condition. The car comes with extensive documentation, clean Carfax report, and service records, making it a desirable collector's item. Key factors for the buyer to consider include the overall originality, exceptional condition, and the included accessories like the owner’s manuals, window sticker, and spare parts. The issue with the airbag light flickering intermittently should be addressed post-purchase. Given the strong interest shown in the bidding section, a reasonable maximum bid for this particular car could be around $13,500 to $14,000. Insights from the comments section highlight the exceptional condition of the car, its desirability among collectors, and the nostalgia associated with Mazda's 1990s lineup. There is mention of the car's stunning appearance, performance characteristics, and unique features specific to the M-Edition Miata. Overall, there is a positive sentiment and genuine appreciation for this well-preserved Mazda Miata.



## Setup

```
yarn install
```

```
yarn index.js
```

(open a new tab in your terminal)

```
touch .env
```

Add `OPENAI_API_KEY=....` with your [OpenAI API key](https://platform.openai.com/api-keys) to your `.env` file

Add the makes & models to the .env file: 
```
MODELS=mazda/miata,porsche/boxster,ford/bronco
```

## Usage

Run for all makes and models specified
```
node analyze.js
```

Or, run for a specific listing
```
URL=https://bringatrailer.com/listing/2000-porsche-911-carrera-cabriolet-33/ price=18000 node analyze.js
```
