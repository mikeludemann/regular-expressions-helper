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

4.2. All countries with shortcuts (Two or three characters) -  (To be continued)

^/\b(af|AF|afg|AFG|ax|AX|ala|ALA|al|AL|alb|ALB|dz|DZ|dza|DZA|as|AS|asm|ASM|ad|AD|and|AND|ao|AO|ago|AGO|ai|AI|aia|AIA|aq|AQ|ata|ATA|ag|AG|atg|ATG|ar|AR|arg|ARG|am|AM|arm|ARM|aw|AW|abw|ABW|au|AU|aus|AUS|at|AT|aut|AUT|az|AZ|aze|AZE|bs|BS|bhs|BHS|bh|BH|bhr|BHR|bd|BD|bgd|BGD|bb|BB|brb|BRB|by|BY|blr|BLR|be|BE|bel|BEL|)\b/$

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