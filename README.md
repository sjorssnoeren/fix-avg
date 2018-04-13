# fix-avg (Work-in-progress)
### Privacywetgeving 2018

#### Cookiemelding en automatisch gegenereerde privacy policy op maat conform AVG 2018 <br/>

*Volledig open-source en geinstalleerd binnen 1 minuut. De catch? Geen, we maken de wereld graag een stukje makkelijker.* 

## Introductie

Vanaf mei is het tijd om je privacy policies weer 'ns flink aan te scherpen. Voor de grotere websites & shops is dit logisch, echter wordt er ook van simpele websites verwacht ditzelfde te doen. Om het je iets makkelijker te maken introduceren we hierbij `fix-avg`, een simpel framework dat je embed op je website. 

Na het toevoegen van dit framework krijg je automatisch de cookie melding met automatisch gegenereerde privacy policy! Geef aan welke modules je wil toepassen en er staat een PDF voor je klaar met je eigen bedrijfsgegevens.

Probeer het zelf! Maximaal 5 minuten werk, dat je een hele hoop tijd en geld kan besparen. You're welcome. Pull requests en verbeteringen zijn van harte welkom.

## Minimale installatie

```html
<script type="text/javascript" src="https://github.com/sjorssnoeren/fix-avg/dist/embedded.js"></script>

<script type="text/javascript">
	createFixAVG({
		policy: {
			modules: ['tracking-pixel', 'google-analytics', 'database'],
			
			contact: {
				companyName: 'The Red Corner B.V.',
				email: 'mail@theredcorner.nl',
				telephone: '+31 (0)76 565 55 11',
				address: 'Ceresplein 145',
				postalCode: '4811CE',
				city: 'Breda',
			},
		},
	});
</script>
```

## Modules

| Naam | Beschrijving |
|------|--------------|
| `tracking-pixel` | Voor tracking-pixels met re-targeting |
| `google-analytics` | Voor implementatie van Google Analytics |

#### Nieuwe module toevoegen?
...

## Geavanceerde Installatie

```html
<script type="text/javascript" src="https://github.com/sjorssnoeren/fix-avg/dist/embedded.js"></script>

<script type="text/javascript">
	createFixAVG({
		policy: {
			modules: ['tracking-pixel', 'google-analytics', 'database'],
			
			contact: {
				companyName: 'The Red Corner B.V.',
				email: 'mail@theredcorner.nl',
				telephone: '+31 (0)76 565 55 11',
				address: 'Ceresplein 145',
				postalCode: '4811CE',
				city: 'Breda',
			},
		},
		
		description: 'Deze website maakt gebruik van cookies om de website te verbeteren. Door verder te gaan binnen onze site, accepteer je automatisch ons cookiebeleid.'
		
		readButton: {
			title: 'Bekijk privacy policy',
			color: 'red'
		},
		
		acceptButton: {
			title: 'Accepteer cookies',
			color: 'red'
		},
	});
</script>
```

## Gebruik met Webpack (UMD)

```
import { createFixAVG } from 'fix-avg';

createFixAVG(...);
```

## License

Gelicenseerd onder MIT, bekijk het LICENSE bestand voor een complete uitleg.
