# regular-expressions-helper

Simple regular expressions for many rules on websites and more

## Examples

```code
1. Numbers

1.1 Whole Numbers

^/[0-9]{0,}/$

1.2 Decimal Numbers

^/[0-9]{0,}[\.\,]{1}[0-9]{0,}/$

1.3 Currency

^/[0-9]{0,}[\.\,]{1}[0-9]{0,2}/$

2. Name

2.1 One Name

^/[a-zA-zäÄöÖüÜ\^\´\`\']{1,}/$

2.2 Full Name (First and Last)

^/[a-zA-zäÄöÖüÜ\^\´\`\']{1,}[\ ]{1}[a-zA-zäÄöÖüÜ\^\´\`\']{1,}/$

2.3 Full Name (First, Middle and Last)

^/[a-zA-zäÄöÖüÜ\^\´\`\']{1,}([\ ]{1}[a-zA-zäÄöÖüÜ\^\´\`\']{1,}){0,}[\ ]{1}[a-zA-zäÄöÖüÜ]{1,}/$

2.4 Full Name (First, Middle, Last and more than one last name)

^/[a-zA-zäÄöÖüÜ\^\´\`\']{1,}([\ ]{1}[a-zA-zäÄöÖüÜ\^\´\`\']{1,}){0,}[\ ]{1}[a-zA-zäÄöÖüÜ\^\´\`\']{1,}/$

^/[a-zA-zäÄöÖüÜ\^\´\`\']{1,}([\ ]{1}[a-zA-zäÄöÖüÜ\^\´\`\']{1,}){0,}[\ ]{1}[a-zA-zäÄöÖüÜ\^\´\`\'\-\ ]{1,}/$

3. Age

^/(([0-9]{1})|([0-9]{2})|([0-9]{3}))/$

3.1 With Conditions

^/(([0-9]{1})|([0-9]{1,2})|([0-9]{1,3}))/$

4. Country Shortcuts

4.1 Simple Shortcuts

^/[a-zA-Z]{2,3}/$

4.2. Only one Country with shortcuts (Example with Germany)

^/\b(de|DE|deu|DEU)\b/$

4.2. All countries with shortcuts (Two and three characters) - (International)

^/\b(af|AF|afg|AFG|ax|AX|ala|ALA|al|AL|alb|ALB|dz|DZ|dza|DZA|as|AS|asm|ASM|ad|AD|and|AND|ao|AO|ago|AGO|ai|AI|aia|AIA|aq|AQ|ata|ATA|ag|AG|atg|ATG|ar|AR|arg|ARG|am|AM|arm|ARM|aw|AW|abw|ABW|au|AU|aus|AUS|at|AT|aut|AUT|az|AZ|aze|AZE|bs|BS|bhs|BHS|bh|BH|bhr|BHR|bd|BD|bgd|BGD|bb|BB|brb|BRB|by|BY|blr|BLR|be|BE|bel|BEL|bz|BZ|blz|BLZ|bj|BJ|ben|BEN|bm|BM|bmu|BMU|bt|BT|btn|BTN|bo|BO|bol|BOL|bq|BQ|bes|BES|ba|BA|bih|BIH|bw|BW|bwa|BWA|bv|BV|bvt|BVT|br|BR|bra|BRA|io|IO|iot|IOT|vg|VG|vgb|VGB|bn|BN|brn|BRN|bg|BG|bgr|BGR|bf|BF|bfa|BFA|bi|BI|bdi|BDI|kh|KH|khm|KHM|cm|CM|cmr|CMR|ca|CA|can|CAN|cv|CV|cpv|CPV|ky|KY|cym|CYM|cf|CF|caf|CAF|td|TD|tcd|TCD|cl|CL|chl|CHL|cn|CN|chn|CHN|cx|CX|cxr|CXR|cc|CC|cck|CCK|co|CO|col|COL|km|KM|com|COM|ck|CK|cok|COK|cr|CR|cri|CRI|hr|HR|hrv|HRV|cu|CU|cub|CUB|cw|CW|cuw|CUW|cy|CY|cyp|CYP|cz|CZ|cze|CZE|cd|CD|cod|COD|dk|DK|dnk|DNK|dj|DJ|dji|DJI|dm|DM|dma|DMA|do|DO|dom|DOM|tl|TL|tls|TLS|ec|EC|ecu|ECU|eg|EG|egy|EGY|sv|SV|slv|SLV|gq|GQ|gnq|GNQ|er|ER|eri|ERI|ee|EE|est|EST|et|ET|eth|ETH|fk|FK|flk|FLK|fo|FO|fro|FRO|fj|FJ|fji|FJI|fi|FI|fin|FIN|fr|FR|fra|FRA|gf|GF|guf|GUF|pf|PF|pyf|PYF|tf|TF|atf|ATF|ga|GA|gab|GAB|gm|GM|gmb|GMB|ge|GE|geo|GEO|de|DE|deu|DEU|gh|GH|gha|GHA|gi|GI|gib|GIB|gr|GR|grc|GRC|gl|GL|grl|GRL|gd|GD|grd|GRD|gp|GP|glp|GLP|gu|GU|gum|GUM|gt|GT|gtm|GTM|gg|GG|ggy|GGY|gn|GN|gin|GIN|gw|GW|gnb|GNB|gy|GY|guy|GUY|ht|HT|hti|HTI|hm|HM|hmd|HMD|hn|HN|hnd|HND|hk|HK|hkg|HKG|hu|HU|hun|HUN|is|IS|isl|ISL|in|IN|ind|IND|id|ID|idn|IDN|ir|IR|irn|IRN|iq|IQ|irq|IRQ|ie|IE|irl|IRL|im|IM|imn|IMN|il|IL|isr|ISR|it|IT|ita|ITA|ci|CI|civ|CIV|jm|JM|jam|JAM|jp|JP|jpn|JPN|je|JE|jey|JEY|jo|JO|jor|JOR|kz|KZ|kaz|KAZ|ke|KE|ken|KEN|ki|KI|kir|KIR|xk|XK|xkx|XKX|kw|KW|kwt|KWT|kg|KG|kgz|KGZ|la|LA|lao|LAO|lv|LV|lva|LVA|lb|LB|lbn|LBN|ls|LS|lso|LSO|lr|LR|lbr|LBR|ly|LY|lby|LBY|li|LI|lie|LIE|lt|LT|ltu|LTU|lu|LU|lux|LUX|mo|MO|mac|MAC|mk|MK|mkd|MKD|mg|MG|mdg|MDG|mw|MW|mwi|MWI|my|MY|mys|MYS|mv|MV|mdv|MDV|ml|ML|mli|MLI|mt|MT|mlt|MLT|mh|MH|mhl|MHL|mq|MQ|mtq|MTQ|mr|MR|mrt|MRT|mu|MU|mus|MUS|yt|YT|myt|MYT|mx|MX|mex|MEX|fm|FM|fsm|FSM|md|MD|mda|MDA|mc|MC|MCO|mn|MN|mng|MNG|me|ME|mne|MNE|ms|MS|msr|MSR|ma|MA|mar|MAR|mz|MZ|moz|MOZ|mm|MM|mmr|MMR|na|NA|nam|NAM|nr|NR|nru|NRU|np|NP|npl|NPL|nl|NL|nld|NDL|an|AN|ant|ANT|nc|NC|ncl|NCL|nz|NZ|nzl|NZL|ni|NI|nic|NIC|ne|NE|ner|NER|ng|NG|nga|NGA|nu|NU|niu|NIU|nf|NF|nfk|NFK|kp|KP|prk|PRK|mp|MP|mnp|MNP|no|NO|nor|NOR|om|OM|omn|OMN|pk|PK|pak|PAK|pw|PW|plw|PLW|ps|PS|pse|PSE|pa|PA|pan|PAN|pg|PG|png|PNG|py|PY|pry|PRY|pe|PE|per|PER|ph|PH|phl|PHL|pn|PN|pcn|PCN|pl|PL|pol|POL|pt|PT|prt|PRT|pr|PR|pri|PRI|qa|QA|qat|QAT|cg|CG|cog|COG|re|RE|reu|REU|ro|RO|rou|ROU|ru|Ru|rus|RUS|rw|RW|rwa|RWA|bl|BL|blm|BLM|sh|SH|shn|SHN|kn|KN|kna|KNA|lc|LC|lca|LCA|mf|MF|maf|MAF|pm|PM|spm|SPM|vc|VC|vct|VCT|ws|WS|wsm|WSM|sm|SM|smr|SMR|st|ST|stp|STP|sa|SA|sau|SUA|sn|SN|sen|SEN|rs|RS|srb|SRB|cs|CS|scg|SCG|sc|SC|syc|SYC|sl|SL|sle|SLE|sg|SG|sgp|SGP|sx|SX|sxm|SXM|sk|SK|svk|SVK|si|SI|svn|SVN|sb|SB|slb|SLB|so|SO|som|SOM|za|ZA|zaf|ZAF|gs|GS|sgs|SGS|kr|KR|kor|KOR|ss|SS|ssd|SSD|es|ES|esp|ESP|lk|LK|lka|LKA|sd|SD|sdn|SDN|sr|SR|sur|SUR|sj|SJ|sjm|SJM|sz|SZ|swz|SWZ|se|SE|swe|SWE|ch|CH|che|CHE|sy|SY|syr|SYR|tw|TW|twn|TWN|tj|TJ|tjk|TJK|tz|TZ|tza|TZA|th|TH|tha|THA|tg|TG|tgo|TGO|tk|TK|tkl|TKL|to|TO|ton|TON|tt|TT|tto|TTO|tn|TN|tun|TUN|tr|TR|tur|TUR|tm|TM|tkm|TKM|tc|TC|tca|TCA|tv|TV|tuv|TUV|vi|VI|vir|VIR|ug|UG|uga|UGA|ua|UA|ukr|UKR|ae|AE|are|ARE|gb|GB|gbr|GBR|us|US|usa|USA|um|UM|umi|UMI|uy|UY|ury|URY|uz|UZ|uzb|UZB|vu|VU|vut|VUT|va|VA|vat|VAT|ve|VE|ven|VEN|vn|VN|vnm|VNM|wf|WF|wlf|WLF|eh|EH|esh|ESH|ye|YE|yem|YEM|zm|ZM|zmb|ZMB|zw|ZW|zwe|ZWE)\b/$

5. Place

^/[a-zA-ZäÄöÖüÜß\'\´\`\-\_\^\ ]{0,}/$

6. Postal Code

^/([0-9]{5}|([a-zA-ZäÄöÖüÜß]{0,3}[\'\´\`\-\_\^\ ]{0,1}[0-9]{5}))/$

7. Street and Number

7.1 Street

^/[0-9a-zA-ZäÄöÖüÜß\'\´\`\-\_\^\ ]{0,}/$

7.2 Number

^/([0-9]{1,}|[0-9]{0,}[\ ]{0,1}[\-]{0,1}[\ ]{0,1}[0-9]{0,}|[0-9]{0,}[a-zA-Z]{0,}[\ ]{0,1}[\-]{0,1}[\ ]{0,1}[0-9]{0,}[a-zA-Z]{0,})/$

8. E-Mail

- ^/(?:[a-z0-9!#$%&'*+/=?^_`{|}~-]+(?:\.[a-z0-9!#$%&'*+/=?^_`{|}~-]+)*|"(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21\x23-\x5b\x5d-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])*")@(?:(?:[a-z0-9](?:[a-z0-9-]*[a-z0-9])?\.)+[a-z0-9](?:[a-z0-9-]*[a-z0-9])?|\[(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?|[a-z0-9-]*[a-z0-9]:(?:[\x01-\x08\x0b\x0c\x0e-\x1f\x21-\x5a\x53-\x7f]|\\[\x01-\x09\x0b\x0c\x0e-\x7f])+)\])/$

9. Passwort (At least a small letter and a big letter and a number and a special character)

- ^/(?=.*?[A-Z])(?=.*?[a-z])(?=.*?[0-9])(?=.*?[#?!@$%^&*-]).{8,}/$

10. Words (Textarea)

- ^/[a-zA-ZäÄöÖüÜ0-9\ \,\.\;\:\-\_\\\(\)\{\)\+\=\?\!\´\`\'\"\&\/\|\§\$\€\@\n]{0,}/$

11. Domains

- ^/(http:\/\/|https:\/\/){0,1}(?!:\/\/)([a-zA-Z0-9-_]+\.)*[a-zA-Z0-9][a-zA-Z0-9-_]+\.[a-zA-Z]{2,11}?/$

12. Date and Time

12.1 Date

12.1.1 Year Month Day - Format

^/([12]\d{3}[\-\/\.]{1}(0[1-9]|1[0-2])[\-\/\.]{1}(0[1-9]|[12]\d|3[01]))/$

12.1.2 Year Day Month - Format

^/([12]\d{3}[\-\/\.]{1}(0[1-9]|[12]\d|3[01])[\-\/\.]{1}(0[1-9]|1[0-2]))/$

12.1.3 Day Month Year - Format

^/((0[1-9]|[12]\d|3[01])[\-\/\.]{1}(0[1-9]|1[0-2])[\-\/\.]{1}[12]\d{3}/$

12.1.4 Month Day Year - Format

^/((0[1-9]|1[0-2])[\-\/\.]{1}(0[1-9]|[12]\d|3[01])[\-\/\.]{1}[12]\d{3})/$

12.2 Time

12.2.1 Hour Minute Second

^/(2[0-3]|[01]?[0-9]):([0-5]?[0-9]):([0-5]?[0-9])/$

12.2.1 Hour Minute Second

^/([0-5]?[0-9]):([0-5]?[0-9]):(2[0-3]|[01]?[0-9])/$
```

## Information

Changes and customization reserved 