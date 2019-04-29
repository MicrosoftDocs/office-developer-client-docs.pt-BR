---
title: Obter informações de amigos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: 'O Outlook Social Connector (OSC) chama o método ISocialProvider:: GetCapabilities para determinar as funcionalidades do provedor do OSC para uma rede social.'
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428792"
---
# <a name="getting-friends-information"></a><span data-ttu-id="ed1ab-103">Obter informações de amigos</span><span class="sxs-lookup"><span data-stu-id="ed1ab-103">Getting friends information</span></span>

<span data-ttu-id="ed1ab-104">O Outlook Social Connector (OSC) chama o método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) para determinar as funcionalidades do provedor do OSC para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="ed1ab-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="ed1ab-105">Se os \*\*\*\* elementos getfriends e **cacheFriends** no XML de **recursos** retornados indicarem que o provedor OSC dá suporte ao recebimento de amigos e ao cache de amigos como itens de contato do Outlook em uma pasta contatos correspondente, o OSC poderá fazer a sequência de chamadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed1ab-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="ed1ab-106">O OSC chama métodos nesta sequência para obter informações e imagens (conforme suportado pela interface [ISocialPerson](isocialpersoniunknown.md) ) para amigos na rede social.</span><span class="sxs-lookup"><span data-stu-id="ed1ab-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ed1ab-107">O OSC atualiza o cache em um intervalo padrão.</span><span class="sxs-lookup"><span data-stu-id="ed1ab-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="ed1ab-108">Se ocorrer um erro durante a atualização do cache, o OSC tentará novamente em outro intervalo predefinido, que também pode ser controlado especificando o elemento **contactSyncRestartInterval** no XML de **recursos** .</span><span class="sxs-lookup"><span data-stu-id="ed1ab-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="ed1ab-109">Para obter mais informações sobre como atualizar o cache de contatos, consulte [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="ed1ab-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="ed1ab-110">[ISocialSession:: LoggedOnUserID](isocialsession-loggedonuserid.md) – o OSC Obtém a ID de usuário do usuário do Office que está conectada à rede social.</span><span class="sxs-lookup"><span data-stu-id="ed1ab-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="ed1ab-111">[ISocialSession:: GetPerson](isocialsession-getperson.md) — usando a ID de usuário do usuário do Office, o OSC Obtém um objeto **ISocialPerson** para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="ed1ab-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="ed1ab-112">[ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) – o OSC Obtém a lista de amigos do usuário na rede social.</span><span class="sxs-lookup"><span data-stu-id="ed1ab-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="ed1ab-113">[ISocialSession:: GetPerson](isocialsession-getperson.md) — para cada pessoa no XML retornado por **GETFRIENDSANDCOLLEAGUES**, o OSC Obtém uma interface **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="ed1ab-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="ed1ab-114">[ISocialPerson:: GetPicture](isocialperson-getpicture.md) — para cada pessoa no XML retornada por **GETFRIENDSANDCOLLEAGUES**, o OSC Obtém um recurso Picture.</span><span class="sxs-lookup"><span data-stu-id="ed1ab-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed1ab-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed1ab-115">See also</span></span>

- [<span data-ttu-id="ed1ab-116">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="ed1ab-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="ed1ab-117">Sequências de chamada típicas do OSC</span><span class="sxs-lookup"><span data-stu-id="ed1ab-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

