---
title: Criando um assunto de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332960"
---
# <a name="creating-a-message-subject"></a><span data-ttu-id="6ad89-103">Criando um assunto de mensagem</span><span class="sxs-lookup"><span data-stu-id="6ad89-103">Creating a Message Subject</span></span>

  
  
<span data-ttu-id="6ad89-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ad89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ad89-105">O assunto de uma mensagem, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), é uma propriedade opcional, usada para resumir a intenção de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="6ad89-105">The subject of a message, **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)), is an optional property, used to summarize the intent of a message.</span></span> <span data-ttu-id="6ad89-106">Se você optar por defini-lo, torná-lo uma cadeia de caracteres de 128 bytes ou menos.</span><span class="sxs-lookup"><span data-stu-id="6ad89-106">If you choose to set it, make it a character string 128 bytes or less.</span></span> <span data-ttu-id="6ad89-107">O limite de 128 byte não é um limite imposto por MAPI; é um limite imposto por alguns provedores de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6ad89-107">The 128 byte limit is not a limit imposed by MAPI; it is a limit imposed by some message store providers.</span></span> <span data-ttu-id="6ad89-108">Para garantir a interoperabilidade com provedores que o impõem, limite os titulares a 128 bytes.</span><span class="sxs-lookup"><span data-stu-id="6ad89-108">To ensure interoperability with providers that do impose it, limit subjects to 128 bytes.</span></span> 
  
<span data-ttu-id="6ad89-109">Esteja ciente de que alguns provedores de armazenamento de mensagens **não permitem PR_SUBJECT** ser gravados em um fluxo com a interface [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ad89-109">Be aware that some message store providers do not allow **PR_SUBJECT** to be written to a stream with the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
  
<span data-ttu-id="6ad89-110">Não definir **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); essa propriedade é definida somente em respostas e mensagens encaminhadas.</span><span class="sxs-lookup"><span data-stu-id="6ad89-110">Do not set **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)); this property is set only on replies and forwarded messages.</span></span> 
  

