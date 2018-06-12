---
title: Obtendo informações de amigos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Outlook Social Connector (OSC) chama o método ISocialProvider::GetCapabilities para determinar os recursos do provedor de OSC para uma rede social.
ms.openlocfilehash: 68443992351f4c83e8e560a753941e97bf91de67
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770821"
---
# <a name="getting-friends-information"></a><span data-ttu-id="71f55-103">Obtendo informações de amigos</span><span class="sxs-lookup"><span data-stu-id="71f55-103">Getting friends information</span></span>

<span data-ttu-id="71f55-104">Outlook Social Connector (OSC) chama o método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) para determinar os recursos do provedor de OSC para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="71f55-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="71f55-105">Se os elementos **getFriends** e **cacheFriends** em **recursos** retornado XML indicarem que o provedor do OSC oferece suporte a introdução de amigos e itens em uma pasta de contatos correspondente de contato de amigos cache como o Outlook, o OSC pode fazer a seguinte sequência de chamada.</span><span class="sxs-lookup"><span data-stu-id="71f55-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="71f55-106">O OSC chama os métodos nesta sequência para obter informações e imagens (conforme suportado pela interface [ISocialPerson](isocialpersoniunknown.md) ) de amigos na rede social.</span><span class="sxs-lookup"><span data-stu-id="71f55-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="71f55-107">O OSC atualiza o cache em um intervalo padrão.</span><span class="sxs-lookup"><span data-stu-id="71f55-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="71f55-108">Se ocorrer um erro durante o cache atualize, as tentativas OSC em outro intervalo predefinido, o que também podem ser controlados especificando-se o elemento **contactSyncRestartInterval** nas **capacidades** XML.</span><span class="sxs-lookup"><span data-stu-id="71f55-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="71f55-109">Para obter mais informações sobre como atualizar o cache de contatos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="71f55-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="71f55-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) — o OSC obtém a identificação de usuário do usuário Office que é conectado à rede social.</span><span class="sxs-lookup"><span data-stu-id="71f55-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="71f55-111">[ISocialSession::GetPerson](isocialsession-getperson.md) — usando a ID de usuário do usuário do Office, o OSC obtém um objeto de **ISocialPerson** para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="71f55-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="71f55-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) — o OSC obtém a lista de amigos do usuário na rede social.</span><span class="sxs-lookup"><span data-stu-id="71f55-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="71f55-113">[ISocialSession::GetPerson](isocialsession-getperson.md) — para cada pessoa no XML retornados por **GetFriendsAndColleagues**, o OSC obtém uma interface **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="71f55-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="71f55-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) — para cada pessoa no XML retornados por **GetFriendsAndColleagues**, o OSC obtém um recurso de imagem.</span><span class="sxs-lookup"><span data-stu-id="71f55-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71f55-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="71f55-115">See also</span></span>

- [<span data-ttu-id="71f55-116">XML para recursos</span><span class="sxs-lookup"><span data-stu-id="71f55-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="71f55-117">Sequências de chamadas comuns do OSC</span><span class="sxs-lookup"><span data-stu-id="71f55-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

