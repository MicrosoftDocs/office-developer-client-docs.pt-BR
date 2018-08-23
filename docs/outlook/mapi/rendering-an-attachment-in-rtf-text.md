---
title: Renderizar um anexo em texto RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5d8fc10f876408d616c5acefb664ba5d61c927a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562971"
---
# <a name="rendering-an-attachment-in-rtf-text"></a><span data-ttu-id="30e77-103">Renderizar um anexo em texto RTF</span><span class="sxs-lookup"><span data-stu-id="30e77-103">Rendering an Attachment in RTF Text</span></span>

  
  
<span data-ttu-id="30e77-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30e77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30e77-105">Formato Rich Text (RTF)-clientes cientes podem recuperar informações de posição de renderização do texto da mensagem RTF observando a seguinte sequência de escape na propriedade de **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem:</span><span class="sxs-lookup"><span data-stu-id="30e77-105">Rich Text Format (RTF)-aware clients can retrieve rendering position information from RTF message text by looking for the following escape sequence in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property:</span></span>
  
 `\objattph`
  
 <span data-ttu-id="30e77-106">**Para localizar as informações de renderização em texto formatado**</span><span class="sxs-lookup"><span data-stu-id="30e77-106">**To locate rendering information in formatted text**</span></span>
  
1. <span data-ttu-id="30e77-107">Chame **IMessage::GetAttachmentTable** para acessar a tabela de anexos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="30e77-107">Call **IMessage::GetAttachmentTable** to access the message's attachment table.</span></span> <span data-ttu-id="30e77-108">Para obter mais informações, consulte [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="30e77-108">For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
2. <span data-ttu-id="30e77-109">Construa uma restrição de propriedade que limita a tabela de linhas que possuem **PR_RENDERING_POSITION** não é igual a -1.</span><span class="sxs-lookup"><span data-stu-id="30e77-109">Build a property restriction that limits the table to rows that have **PR_RENDERING_POSITION** not equal to -1.</span></span> <span data-ttu-id="30e77-110">Para obter mais informações, consulte **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="30e77-110">For more information, see **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="30e77-111">Chame **IMAPITable:: Restrict** para impor a restrição.</span><span class="sxs-lookup"><span data-stu-id="30e77-111">Call **IMAPITable::Restrict** to enforce the restriction.</span></span> <span data-ttu-id="30e77-112">Para obter mais informações, consulte [IMAPITable:: Restrict](imapitable-restrict.md).</span><span class="sxs-lookup"><span data-stu-id="30e77-112">For more information, see [IMAPITable::Restrict](imapitable-restrict.md).</span></span>
    
4. <span data-ttu-id="30e77-113">Chame **IMAPITable:: SortTable** para classificar os anexos.</span><span class="sxs-lookup"><span data-stu-id="30e77-113">Call **IMAPITable::SortTable** to sort the attachments.</span></span> <span data-ttu-id="30e77-114">Para obter mais informações, consulte [IMAPITable:: SortTable](imapitable-sorttable.md).</span><span class="sxs-lookup"><span data-stu-id="30e77-114">For more information, see [IMAPITable::SortTable](imapitable-sorttable.md).</span></span>
    
5. <span data-ttu-id="30e77-115">Chame **IMAPITable:: QueryRows** para recuperar as linhas apropriadas.</span><span class="sxs-lookup"><span data-stu-id="30e77-115">Call **IMAPITable::QueryRows** to retrieve the appropriate rows.</span></span> <span data-ttu-id="30e77-116">Para obter mais informações, consulte [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="30e77-116">For more information, see [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
    
6. <span data-ttu-id="30e77-117">Chame o método de **IMAPIProp::OpenProperty** da mensagem para recuperar **PR_RTF_COMPRESSED** com a interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="30e77-117">Call the message's **IMAPIProp::OpenProperty** method to retrieve **PR_RTF_COMPRESSED** with the **IStream** interface.</span></span> <span data-ttu-id="30e77-118">Para obter mais informações, consulte [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="30e77-118">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
    
7. <span data-ttu-id="30e77-119">Examinar o fluxo, procurando por espaço reservado renderização, `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="30e77-119">Scan the stream, looking for the rendering placeholder,  `\objattph`.</span></span> <span data-ttu-id="30e77-120">O caractere seguinte este espaço reservado é o local para o próximo anexo na tabela classificada.</span><span class="sxs-lookup"><span data-stu-id="30e77-120">The character following this placeholder is the place for the next attachment in the sorted table.</span></span>
    

