---
title: Criando um assunto da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 419c9776b380436b1a7163803a8677fb6a89be97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766364"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="cb951-103">Criando um assunto da mensagem</span><span class="sxs-lookup"><span data-stu-id="cb951-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="cb951-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb951-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb951-105">O assunto de uma mensagem, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), é uma propriedade opcional, usada para resumir a intenção de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="cb951-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="cb951-106">Se você optar por defini-la, tornam uma cadeia de caracteres 128 bytes ou menos.</span><span class="sxs-lookup"><span data-stu-id="cb951-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="cb951-107">O limite de 128 bytes não é um limite imposto pelo MAPI; é um limite imposto por alguns provedores de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="cb951-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="cb951-108">Para assegurar a interoperabilidade com provedores que impõem-lo, limite assuntos a 128 bytes.</span><span class="sxs-lookup"><span data-stu-id="cb951-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="cb951-109">Lembre-se de que alguns provedores de armazenamento de mensagem não permita **PR_SUBJECT** a serem gravados em um stream com a interface [IStream](http://msdn.microsoft.com/pt-br/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cb951-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](http://msdn.microsoft.com/pt-br/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="cb951-110">Não definir **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); Essa propriedade é definida somente em respostas e mensagens encaminhada.</span><span class="sxs-lookup"><span data-stu-id="cb951-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

