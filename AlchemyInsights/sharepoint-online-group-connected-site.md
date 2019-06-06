---
title: Dodavanje grupe web-mjesta sustava SharePoint
ms.author: kirks
author: Techwriter40
manager: pamgreen
ms.audience: Admin
ms.topic: article
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.collection: Adm_O365
ms.custom: ''
ms.assetid: f7d730bf-0d6e-424c-970c-6137c71cb50b
ms.openlocfilehash: 352bad1b8fe219f95a37c9ac268c6c4dd8801dfc
ms.sourcegitcommit: 6d341637dbb14e90726a1ce1d68f077ace9bb765
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/04/2019
ms.locfileid: "34719474"
---
# <a name="create-group-connected-site-in-sharepoint-online"></a><span data-ttu-id="c83c4-102">Stvaranje grupe povezanih web-mjesta u SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c83c4-102">Create group connected site in SharePoint Online</span></span>

<p><span data-ttu-id="c83c4-103"><strong>Postoji nekoliko uobičajenih problema naišao je na prilikom stvaranja ili ponovno stvaranje grupe povezani web-mjesta.&nbsp;</strong></span><span class="sxs-lookup"><span data-stu-id="c83c4-103"><strong>There are a couple of common issues encountered when creating or re-creating a group connected site.&nbsp;</strong></span></span></p>  <p><span data-ttu-id="c83c4-104">1.Ako ste izbrisali grupu i njegovih povezanih web-mjesta i želite stvoriti drugu web-mjesta s istim URL, morat ćete trajno ukloniti prethodno web-mjesto.</span><span class="sxs-lookup"><span data-stu-id="c83c4-104">1. If you have deleted a group and its connected site and wish to create another site with the same URL, you'll need to permanently remove the previous site.</span></span></p>  <ul>  <li><span data-ttu-id="c83c4-105">Preuzmite <a title="SPO upravljanja ljuske</span><span class="sxs-lookup"><span data-stu-id="c83c4-105">Download <a title="SPO Management Shell</span></span>" href="https://support.office.com/en-ie/article/introduction-to-the-sharepoint-online-management-shell-c16941c3-19b4-4710-8056-34c034493429"><span data-ttu-id="c83c4-106">Ljuske za upravljanje SPO</a> - dodatne informacije na powershell Uvod u odjeljku <a title="Uvod u SharePoint Online ljuske za upravljanje</span><span class="sxs-lookup"><span data-stu-id="c83c4-106">SPO Management Shell</a> - For more info on getting started with powershell, see <a title="Getting started with SharePoint Online Management Shell</span></span>" href="https://docs.microsoft.com/en-us/powershell/module/sharepoint-online/remove-sposite?view=sharepoint-ps"><span data-ttu-id="c83c4-107">Uvod u SharePoint Online ljuske za upravljanje</a>.</span><span class="sxs-lookup"><span data-stu-id="c83c4-107">Getting started with SharePoint Online Management Shell</a>.</span></span> <br /><br /></li>  <li><span data-ttu-id="c83c4-108">Uklanjanje web-mjesta iz izbrisane web-mjesta pomoću u <a title="Ukloni SPODeletedSite</span><span class="sxs-lookup"><span data-stu-id="c83c4-108">Remove the Site from Deleted Sites using the <a title="Remove-SPODeletedSite</span></span>" href="https://docs.microsoft.com/en-us/powershell/module/sharepoint-online/remove-sposite?view=sharepoint-ps"><span data-ttu-id="c83c4-109">Ukloni SPODeletedSite</a> powershell cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c83c4-109">Remove-SPODeletedSite</a> powershell cmdlet.</span></span></li>  </ul>  <p><span data-ttu-id="c83c4-110">Ako izradi grupe povezanih web-mjesta i primiti upozorenje <strong>'drugu grupu s iste alias već postoji'</strong>, provjerite postojeće grupe iz u <a title="iz centra za administraciju sistema Office 365</span><span class="sxs-lookup"><span data-stu-id="c83c4-110">If you're creating a group connected site and receive a warning <strong>'Another group with the same alias already exists'</strong>, check the existing groups from the <a title="Office 365 from the Admin Center</span></span>" href="https://admin.microsoft.com/Adminportal/Home?source=applauncher#/groups"><span data-ttu-id="c83c4-111">Office 365 iz centra za administraciju</a>.</span><span class="sxs-lookup"><span data-stu-id="c83c4-111">Office 365 from the Admin Center</a>.</span></span> <span data-ttu-id="c83c4-112">Da biste riješili taj problem, izbrišite postojeće grupe ako više nije potrebna ili stvaranje web-mjesta s različitim Pseudonim dodijeljen.&nbsp;</span><span class="sxs-lookup"><span data-stu-id="c83c4-112">To resolve the issue, delete the existing group if it's no longer needed or create the site with a different alias assigned.&nbsp;</span></span></p>  <p><span data-ttu-id="c83c4-113"><strong>Stvaranje i korištenje Moderna grupe s SharePoint na različite načina.&nbsp;</strong></span><span class="sxs-lookup"><span data-stu-id="c83c4-113"><strong>There are different ways to create and use modern groups with SharePoint.&nbsp;</strong></span></span></p>  <ol>  <li><span data-ttu-id="c83c4-114">Postojeća web-mjesta možete se povezati s Office 365 grupe.</span><span class="sxs-lookup"><span data-stu-id="c83c4-114">You can connect existing sites to an Office 365 group.</span></span> <span data-ttu-id="c83c4-115">Za dodatne informacije pogledajte <a title="povezivanje programa Office 365 grupu pomoću SharePoint ineterface korisnika</span><span class="sxs-lookup"><span data-stu-id="c83c4-115">For more info, see <a title="Connect an Office 365 group using the SharePoint user ineterface</span></span>" href="https://docs.microsoft.com/en-us/sharepoint/dev/transform/modernize-connect-to-office365-group#connect-an-office-365-group-using-the-sharepoint-user-interface"><span data-ttu-id="c83c4-116">Povezivanje programa Office 365 grupu pomoću SharePoint ineterface korisnika</a>.</span><span class="sxs-lookup"><span data-stu-id="c83c4-116">Connect an Office 365 group using the SharePoint user ineterface</a>.</span></span></li>  <li><span data-ttu-id="c83c4-117">Da biste stvorili programa Office 365 grupe povezanih web-mjesta, trebat ćete stvoriti web-mjesto tima.</span><span class="sxs-lookup"><span data-stu-id="c83c4-117">To create an Office 365 group connected site, you'll need to create a Team Site.</span></span> <span data-ttu-id="c83c4-118">Za dodatne informacije pogledajte <a title="stvorite web-mjesto tima u SharePoint</span><span class="sxs-lookup"><span data-stu-id="c83c4-118">For more info, see <a title="Create a team site in SharePoint</span></span>" href="https://support.office.com/en-us/article/create-a-team-site-in-sharepoint-ef10c1e7-15f3-42a3-98aa-b5972711777d"><span data-ttu-id="c83c4-119">Stvorite web-mjesto tima u SharePoint.</a></span><span class="sxs-lookup"><span data-stu-id="c83c4-119">Create a team site in SharePoint.</a></span></span></li>  </ol>
