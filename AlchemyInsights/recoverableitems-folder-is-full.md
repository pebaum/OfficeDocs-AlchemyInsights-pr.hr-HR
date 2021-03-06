---
title: 1336 Mapa RecoverableItems je puna
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: 04/21/2020
ms.audience: ITPro
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.custom:
- "1336"
- "3700003"
ms.assetid: a3a923e8-fece-4a26-b8b6-00970d75275e
ms.openlocfilehash: 4f0cba480fcc05114abd8f370b84e9a37e5f2804
ms.sourcegitcommit: bc7d6f4f3c9f7060d073f5130e1ec856e248d020
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/02/2020
ms.locfileid: "44510744"
---
# <a name="the-recoverable-items-folder-is-full"></a>Mapa Oporavljene stavke puna je

Za poštanske sandučiće sustava Exchange Online zadano ograničenje pohrane za mapu Stavke koje se mogu oporaviti iznosi 30 GB. Ograničenje prostora za pohranu mape Oporavljene stavke automatski se povećava na 100 GB ako je poštanski sandučić postavljen na čuvanje litigation, čuvanje predočavanja elektroničkih dokumenata ili je dodijeljeno pravilima zadržavanja.

Kada mapa Oporavljene stavke dosegne ograničenje pohrane, funkcija poštanskog sandučića utječe na sljedeće načine:

- Korisnik ne može izbrisati stavke iz poštanskog sandučića.

- Pomoćnik za upravljane mape ne može izbrisati stavke na temelju oznake zadržavanja ili postavki upravljanih mapa.

- Za poštanske sandučiće koji imaju omogućen oporavak jedne stavke ili su stavljeni na čekanje, postupak zaštite stranice za kopiranje na zapis ne može održavati verzije stavki koje je uredio korisnik.

- Za poštanske sandučiće koji imaju omogućeno zapisivanje nadzora poštanskog sandučića, u podmapu Nadzor stavke koje se mogu spremiti nije moguće spremiti nikakve stavke poštanskog sandučića.

Za poštanske sandučiće koji nisu na čekanju administratori mogu koristiti `Search-Mailbox -SearchDumpsterOnly -DeleteContent` naredbu u powershellu exchange online za brisanje stavki u mapi Stavke koje se mogu oporaviti. Dodatne informacije potražite u sljedećim temama:

- [Traženje i brisanje poruka](https://docs.microsoft.com/microsoft-365/compliance/search-for-and-delete-messagesadmin-help)

- [Poštanski sandučić za pretraživanje](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Search-Mailbox)

Za poštanske sandučiće koji su na čekanju administratori moraju ukloniti čekanje da bi mogli izbrisati stavke iz mape Stavke koje se mogu oporaviti. Dodatne informacije [potražite u odjeljku Brisanje stavki u mapi Stavke koje se mogu oporaviti poštanskih sandučića u oblaku na čekanju](https://docs.microsoft.com/microsoft-365/compliance/delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold).

Da bi spriječili da mapa Oporavljene stavke postane puna, administratori mogu povećati ograničenje pohrane mape Stavke koje se mogu oporaviti za poštanske sandučiće na čekanju i postaviti pravila zadržavanja poštanskog sandučića koja premješta stavke iz mape Stavke koje se mogu oporaviti u poštanski sandučić arhive korisnika. Pogledajte [Povećanje kvote Oporavljenih stavki za poštanske sandučiće na čekanju](https://docs.microsoft.com/microsoft-365/compliance/increase-the-recoverable-quota-for-mailboxes-on-hold).
