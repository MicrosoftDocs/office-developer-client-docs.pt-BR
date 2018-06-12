---
title: Sobre configurações antispam
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 04e00e49-c12d-4517-8574-410741d0fa06
description: Outlook permite que os usuários especifiquem configurações para cada conta para ajudar a proteger a conta contra spam. Tais configurações antispam são armazenadas em uma seção designada para essa conta no perfil do usuário.
ms.openlocfilehash: 9d1ad6fcc0748d57dd71cb80460705fcd176fae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765779"
---
# <a name="about-anti-spam-settings"></a><span data-ttu-id="c3553-104">Sobre configurações antispam</span><span class="sxs-lookup"><span data-stu-id="c3553-104">About anti-spam settings</span></span>

<span data-ttu-id="c3553-105">Outlook permite que os usuários especifiquem configurações para cada conta para ajudar a proteger a conta contra spam.</span><span class="sxs-lookup"><span data-stu-id="c3553-105">Outlook allows users to specify settings for each account to help protect the account from spam.</span></span> <span data-ttu-id="c3553-106">Tais configurações antispam são armazenadas em uma seção designada para essa conta no perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="c3553-106">Such anti-spam settings are stored in a section designated for that account in the user's profile.</span></span> <span data-ttu-id="c3553-107">Use a propriedade [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) para obter o ID exclusivo (UID) para a seção no perfil que armazena as preferências do usuário para essa conta, incluindo as configurações antispam.</span><span class="sxs-lookup"><span data-stu-id="c3553-107">Use the [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) property to obtain the unique ID (UID) for the section in the profile that stores the user's preferences for this account, including the anti-spam settings.</span></span> 
  
<span data-ttu-id="c3553-108">Use as propriedades a seguir para obter configurações antispam para a conta:</span><span class="sxs-lookup"><span data-stu-id="c3553-108">Use the following properties to obtain anti-spam settings for the account:</span></span>
  
- <span data-ttu-id="c3553-109">[PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)— Especifica uma lista delimitada por ponto e vírgula dos endereços de email e domínios que o usuário especificou como remetentes bloqueados para a conta.</span><span class="sxs-lookup"><span data-stu-id="c3553-109">[PidTagSpamJunkSenders](http://msdn.microsoft.com/library/3c5182a7-7d7a-48e8-b9cb-5abd7739f0fd%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as blocked senders for the account.</span></span>
    
- <span data-ttu-id="c3553-110">[PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)— Especifica o nível de filtragem de spam que o usuário tiver especificado para a conta.</span><span class="sxs-lookup"><span data-stu-id="c3553-110">[PidTagSpamThreshold](http://msdn.microsoft.com/library/2b2d6b8e-e3dd-4a9b-8bb5-53add675605d%28Office.15%29.aspx)—Specifies the level of spam-filtering that the user has specified for the account.</span></span> <span data-ttu-id="c3553-111">A tabela a seguir mostra os valores com suporte.</span><span class="sxs-lookup"><span data-stu-id="c3553-111">The following table shows the supported values.</span></span>
    
|<span data-ttu-id="c3553-112">Valor com suporte</span><span class="sxs-lookup"><span data-stu-id="c3553-112">Supported value</span></span> |<span data-ttu-id="c3553-113">Definição</span><span class="sxs-lookup"><span data-stu-id="c3553-113">Definition</span></span> |
|:-----|:-----|
|<span data-ttu-id="c3553-114">None</span><span class="sxs-lookup"><span data-stu-id="c3553-114">None</span></span>  <br/> |<span data-ttu-id="c3553-115">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="c3553-115">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="c3553-116">Baixa</span><span class="sxs-lookup"><span data-stu-id="c3553-116">Low</span></span>  <br/> |<span data-ttu-id="c3553-117">0x00000006</span><span class="sxs-lookup"><span data-stu-id="c3553-117">0x00000006</span></span>  <br/> |
|<span data-ttu-id="c3553-118">Médio</span><span class="sxs-lookup"><span data-stu-id="c3553-118">Medium</span></span>  <br/> |<span data-ttu-id="c3553-119">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c3553-119">0x00000005</span></span>  <br/> |
|<span data-ttu-id="c3553-120">Alta</span><span class="sxs-lookup"><span data-stu-id="c3553-120">High</span></span>  <br/> |<span data-ttu-id="c3553-121">0x00000003</span><span class="sxs-lookup"><span data-stu-id="c3553-121">0x00000003</span></span>  <br/> |
   
- <span data-ttu-id="c3553-122">[PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)— Especifica uma lista delimitada por ponto e vírgula dos endereços de email e domínios que o usuário especificou como destinatários confiáveis para a conta.</span><span class="sxs-lookup"><span data-stu-id="c3553-122">[PidTagSpamTrustedRecipients](http://msdn.microsoft.com/library/59f43316-3ff6-4ed0-bc29-b31039192b08%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted recipients for the account.</span></span>
    
- <span data-ttu-id="c3553-123">[PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)— Especifica uma lista delimitada por ponto e vírgula dos endereços de email e domínios que o usuário especificou como remetentes confiáveis para a conta.</span><span class="sxs-lookup"><span data-stu-id="c3553-123">[PidTagSpamTrustedSenders](http://msdn.microsoft.com/library/8e3f0094-e64b-4828-ba8f-5eed35f85366%28Office.15%29.aspx)—Specifies a semicolon-delimited list of email addresses and domains that the user has specified as trusted senders for the account.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c3553-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3553-124">See also</span></span>

- [<span data-ttu-id="c3553-125">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="c3553-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="c3553-126">Adicionar os nomes das listas de filtro de lixo eletrônico</span><span class="sxs-lookup"><span data-stu-id="c3553-126">Add names to the Junk Email Filter lists</span></span>](http://office.microsoft.com/en-us/outlook-help/add-names-to-the-junk-email-filter-lists-HA010355043.aspx?CTT=1)

