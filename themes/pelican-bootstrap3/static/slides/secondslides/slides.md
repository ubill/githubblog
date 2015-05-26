% Habits
% John Doe
% March 22, 2005

# In the morning

## Getting up

- Turn off alarm
- Get out of bed
- Producing slide shows with Pandoc:
- http://pandoc.org/demo/example9/producing-slide-shows-with-pandoc.html

## Breakfast

- Eat eggs
- Drink coffee

# In the evening

## Adding some source code here. (Haskell)

~~~~ {#mycode .haskell .numberLines startFrom="100"}
qsort []     = []
qsort (x:xs) = qsort (filter (< x) xs) ++ [x] ++
               qsort (filter (>= x) xs)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## Moar code. (Javascript)

~~~~ {#mycode .javascript .numberLines}
for (var i=0; i < data.length; i++) {
  totalTemperature = 0;

  for (var j=0; j < data[i].temperatures.length; j++) {
    totalTemperature += data[i].temperatures[j];
  }

  averageTemperature = totalTemperature / data[i].temperatures.length;

  coords.push([averageTemperature, data[i].population]);
}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## Dinner

- Eat spaghetti
- Drink wine

------------------

![picture of spaghetti](/theme/slides/secondslides/images/spaghetti.jpg)

## Going to sleep

- Get in bed
- Count sheep
