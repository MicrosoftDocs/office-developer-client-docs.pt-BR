---
title: Renderização de um anexo em texto RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439790"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="6f97f-103">Renderização de um anexo em texto RTF</span><span class="sxs-lookup"><span data-stu-id="6f97f-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="6f97f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f97f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f97f-105">Clientes com conhecimento em RTF (Rich Text Format) podem recuperar informações de posição de renderização do texto da mensagem RTF procurando a seguinte sequência de escape na propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem:</span><span class="sxs-lookup"><span data-stu-id="6f97f-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="6f97f-106">**Para localizar informações de renderização em texto formatado**</span><span class="sxs-lookup"><span data-stu-id="6f97f-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="6f97f-107">Chame **IMessage::GetAttachmentTable** para acessar a tabela de anexos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f97f-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="6f97f-108">Para obter mais informações, consulte [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="6f97f-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="6f97f-109">Crie uma restrição de propriedade que limite a tabela a linhas que não **PR_RENDERING_POSITION** igual a -1.</span><span class="sxs-lookup"><span data-stu-id="6f97f-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="6f97f-110">Para obter mais informações, **consulte PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6f97f-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="6f97f-111">Chame **IMAPITable::Restrict** para impor a restrição.</span><span class="sxs-lookup"><span data-stu-id="6f97f-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="6f97f-112">Para obter mais informações, consulte [IMAPITable::Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="6f97f-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="6f97f-113">Chame **IMAPITable::SortTable** para classificar os anexos.</span><span class="sxs-lookup"><span data-stu-id="6f97f-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="6f97f-114">Para obter mais informações, consulte [IMAPITable::SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="6f97f-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="6f97f-115">Chame **IMAPITable::QueryRows** para recuperar as linhas apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6f97f-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="6f97f-116">Para obter mais informações, [consulte IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="6f97f-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="6f97f-117">Chame o método **IMAPIProp::OpenProperty** da mensagem para recuperar PR_RTF_COMPRESSED **com** a interface **IStream.**</span><span class="sxs-lookup"><span data-stu-id="6f97f-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="6f97f-118">Para obter mais informações, [consulte IMAPIProp::OpenProperty](imapiprop-openproperty.md) e **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="6f97f-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="6f97f-119">Digitalizar o fluxo, procurando o espaço reservado de renderização,  `\objattph` .</span><span class="sxs-lookup"><span data-stu-id="6f97f-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="6f97f-120">O caractere após esse espaço reservado é o lugar para o próximo anexo na tabela ordenada.</span><span class="sxs-lookup"><span data-stu-id="6f97f-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

