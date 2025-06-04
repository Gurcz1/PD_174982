# 📚 Haskell – Ściągawka przed kolokwium

## ✅ 1. Rekurencja

```haskell
dodaj1 :: [Int] -> [Int]
dodaj1 [] = []
dodaj1 (x:xs) = (x + 1) : dodaj1 xs
```

---

## ✅ 2. `map`

```haskell
pomnoz2 :: Int -> Int
pomnoz2 x = x * 2

listaPomnozona :: [Int] -> [Int]
listaPomnozona xs = map pomnoz2 xs
```

---

## ✅ 3. List comprehension (bez warunku)

```haskell
kwadraty :: [Int] -> [Int]
kwadraty xs = [x * x | x <- xs]
```

---

## ✅ 4. List comprehension z kwalifikatorem

```haskell
tylkoParzyste :: [Int] -> [Int]
tylkoParzyste xs = [x | x <- xs, even x]
```

---

## ✅ 5. Złożone list comprehension

```haskell
[x + y | x <- [1..2], y <- [1..x]]
-- wynik: [2,3,4]

[x * y | x <- [3,2,1], y <- [1..x]]
-- wynik: [3,6,9,2,4,1]
```

---

## ✅ 6. Guardy (`|`)

```haskell
opis :: Int -> String
opis x
  | x < 0     = "ujemna"
  | x == 0    = "zero"
  | x < 10    = "mala"
  | otherwise = "duza"
```

---

## ✅ 7. `if then else`

```haskell
czyParzysta :: Int -> String
czyParzysta x = if x `mod` 2 == 0 then "parzysta" else "nieparzysta"
```

---

## ✅ 8. XOR – logika

```haskell
xor :: Bool -> Bool -> Bool
xor x y
  | x == y    = False
  | otherwise = True
```

---

## ✅ 9. Łączenie list

```haskell
[1,2] ++ [3,4]       -- [1,2,3,4]
1 : [2,3]            -- [1,2,3]
```

---

## ✅ 10. Skróty i wbudowane funkcje

| Symbol / Funkcja | Znaczenie                 |
|------------------|---------------------------|
| `:`              | dodaj element na początek listy |
| `++`             | połącz dwie listy         |
| `<-`             | generator w list comp.    |
| `mod`            | reszta z dzielenia        |
| `even`           | czy liczba jest parzysta  |

---

💡 Powodzenia na kolosie! Masz to w małym palcu 😎