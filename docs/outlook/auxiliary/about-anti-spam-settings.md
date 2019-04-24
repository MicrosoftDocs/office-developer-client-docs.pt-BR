---
title: Sobre as configurações antispam
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: O Outlook permite aos usuários especificar configurações para cada conta a fim de protegê-la contra spam. Essas configurações antispam são armazenadas em uma seção designada para essa conta no perfil de usuário.
ms.openlocfilehash: cf9bce058e9e0bd1c8f6f14637ae0af73f155940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316956"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="7d3ba-104">Sobre as configurações antispam</span><span class="sxs-lookup"><span data-stu-id="7d3ba-104">About anti-spam settings</span></span>

<span data-ttu-id="7d3ba-105">O Outlook permite aos usuários especificar configurações para cada conta a fim de protegê-la contra spam.</span><span class="sxs-lookup"><span data-stu-id="7d3ba-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="7d3ba-106">Essas configurações antispam são armazenadas em uma seção designada para essa conta no perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="7d3ba-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="7d3ba-107">Use a propriedade [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) para obter a ID exclusiva (UID) da seção no perfil que armazena as preferências do usuário para essa conta, incluindo as configurações antispam.</span><span class="sxs-lookup"><span data-stu-id="7d3ba-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="7d3ba-108">Use as seguintes propriedades para obter as configurações antispam da conta:</span><span class="sxs-lookup"><span data-stu-id="7d3ba-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="7d3ba-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx): especifica uma lista de endereços de email e domínios separados por ponto e vírgula que o usuário especificou como remetentes bloqueados da conta.</span><span class="sxs-lookup"><span data-stu-id="7d3ba-109">[PidTagSpamJunkSenders](https://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="7d3ba-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx): especifica o nível de filtragem de spam que o usuário especificou para a conta.</span><span class="sxs-lookup"><span data-stu-id="7d3ba-110">[PidTagSpamThreshold](https://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="7d3ba-111">A tabela a seguir mostra os valores compatíveis.</span><span class="sxs-lookup"><span data-stu-id="7d3ba-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="7d3ba-112">Valor compatível</span><span class="sxs-lookup"><span data-stu-id="7d3ba-112">Supported value</span></span> |<span data-ttu-id="7d3ba-113">Definição</span><span class="sxs-lookup"><span data-stu-id="7d3ba-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="7d3ba-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7d3ba-114">None</span></span>  <br/> |<span data-ttu-id="7d3ba-115">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="7d3ba-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="7d3ba-116">Baixo</span><span class="sxs-lookup"><span data-stu-id="7d3ba-116">Low</span></span>  <br/> |<span data-ttu-id="7d3ba-117">0x00000006</span><span class="sxs-lookup"><span data-stu-id="7d3ba-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="7d3ba-118">Médio</span><span class="sxs-lookup"><span data-stu-id="7d3ba-118">Medium</span></span>  <br/> |<span data-ttu-id="7d3ba-119">0x00000005</span><span class="sxs-lookup"><span data-stu-id="7d3ba-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="7d3ba-120">Alto</span><span class="sxs-lookup"><span data-stu-id="7d3ba-120">High</span></span>  <br/> |<span data-ttu-id="7d3ba-121">0x00000003</span><span class="sxs-lookup"><span data-stu-id="7d3ba-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="7d3ba-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx): especifica uma lista de endereços de email e domínios separados por ponto e vírgula que o usuário especificou como destinatários confiáveis da conta.</span><span class="sxs-lookup"><span data-stu-id="7d3ba-122">[PidTagSpamTrustedRecipients](https://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="7d3ba-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx): especifica uma lista de endereços de email e domínios separados por ponto e vírgula que o usuário especificou como remetentes confiáveis da conta.</span><span class="sxs-lookup"><span data-stu-id="7d3ba-123">[PidTagSpamTrustedSenders](https://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d3ba-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d3ba-124">See also</span></span>

- [<span data-ttu-id="7d3ba-125">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="7d3ba-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="7d3ba-126">Adicionar nomes às listas de filtros de lixo eletrônico</span><span class="sxs-lookup"><span data-stu-id="7d3ba-126">Add names to the Junk Email Filter lists</span></span>](https://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

