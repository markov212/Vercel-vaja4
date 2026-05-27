# Projektna vaja - IT nadzorna plošča (Vercel in Supabase)

## Kratek opis
Ta projekt je enostavna statusna stran (nadzorna plošča) za spremljanje delovanja strežnikov. Narejena je v enem kosu (HTML, CSS in JavaScript so skupaj v index.html), tako da se stran hitreje naloži in je lažja za vzdrževanje. Na strani je tudi gumb, ki simulira mrežni test (ping) in izpiše odzivni čas v milisekundah.

## Kaj sem uporabil od tehnologij?
- HTML za osnovno strukturo strani
- CSS za temen dizajn (dark mode)
- JavaScript za delovanje mrežnega testa (gumb)
- GitHub za shranjevanje kode in verzij
- Vercel za avtomatsko objavo spletne strani na internetu
- Supabase za nastavitve zunanje baze podatkov

## Povezave do strani
- Glavna stran (Production): https://vercel-vaja4.vercel.app
- Testna stran (Preview): https://vercel-vaja4-git-markov212-patch-1-marko-v.vercel.app/

## Kako deluje CI/CD v mojem projektu?
Vse skupaj je nastavljeno tako, da poteka avtomatsko. Ko na računalniku ali direktno na GitHubu popravim kodo in potrdim spremembe (commit/push), Vercel to takoj sam opazi. Samodejno potegne novo kodo, jo osveži in v par sekundah je nova verzija strani že živo na internetu, brez da bi moral jaz ročno nalagati datoteke na strežnik.

## Zunanja konfiguracija (Supabase baza)
V sklopu vaje sem si na platformi Supabase ustvaril bazo in tabelo z imenom "messages". Tabela je pripravljena za shranjevanje sistemskih logov ali sporočil. 

Na tabeli sem vklopil RLS (Row Level Security) zaščito in dodal osnovno pravilo "Allow public read", kar pomeni, da lahko kdor koli bere podatke, za resno pisanje v bazo pa bi v praksi potrebovali zaklenjene račune zaradi varnosti pred spamom.

## Težave, ki sem jih imel
Na začetku mi stran ni delovala, ker se je Vercel nekaj zatikal okoli imen datotek in mi je javljal napako 404. Težavo sem rešil tako, da sem vse skupaj združil v eno glavno datoteko index.html, kar je Vercel takoj pravilno prebral. Druga manjša težava je bila s cachingom v brskalniku, saj po posodobitvi nisem takoj videl sprememb, kar sem rešil s testiranjem v Incognito načinu.
