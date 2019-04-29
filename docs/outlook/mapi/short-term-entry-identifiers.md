---
title: Identificadores de entradas de curto prazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1b361e025b631418eb63c5c74da264beadec2974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439559"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="78955-103">Identificadores de entradas de curto prazo</span><span class="sxs-lookup"><span data-stu-id="78955-103">Short-term entry identifiers</span></span>

<span data-ttu-id="78955-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78955-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78955-105">Um identificador de entrada de curto prazo é atribuído por um provedor de serviços a um objeto quando o identificador deve ser construído rapidamente e não precisa durar ao longo do tempo ou da distância.</span><span class="sxs-lookup"><span data-stu-id="78955-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="78955-106">A exclusividade de um identificador de entrada de curto prazo é garantido apenas pela vida da sessão atual na estação de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="78955-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="78955-107">Normalmente, um identificador de entrada de curto prazo só é válido até que o objeto que ele representa seja liberado.</span><span class="sxs-lookup"><span data-stu-id="78955-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="78955-108">Os identificadores de entrada de curto prazo são atribuídos às linhas nas tabelas e às entradas nas caixas de diálogo, onde é necessário fornecer dados rapidamente para navegação.</span><span class="sxs-lookup"><span data-stu-id="78955-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="78955-109">Por exemplo, os provedores de repositórios de mensagens atribuem identificadores de entrada de curto prazo a linhas de mensagens em uma tabela de conteúdo e a destinatários em uma tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="78955-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="78955-110">Os clientes podem usar esses identificadores de entrada de curto prazo para abrir os objetos representados pelas linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="78955-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="78955-111">No enTanto, ao contrário de identificadores de entrada de longo prazo, que podem ser usados com qualquer um dos métodos **OpenEntry** , os identificadores de entrada de curto prazo devem ser usados com o método **OpenEntry** do contêiner.</span><span class="sxs-lookup"><span data-stu-id="78955-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="78955-112">Implementando identificadores de entrada de curto prazo</span><span class="sxs-lookup"><span data-stu-id="78955-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="78955-113">As maneiras mais comuns de implementar identificadores de entrada de curto prazo incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="78955-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="78955-114">Fazer com que os identificadores de entrada de curto prazo sejam iguais aos identificadores de longo prazo, deixando todos os sinalizadores desdefinidas.</span><span class="sxs-lookup"><span data-stu-id="78955-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="78955-115">Fazer os identificadores de entrada de curto prazo diferentes dos identificadores de longo prazo, definindo todos os sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="78955-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="78955-116">Os clientes podem identificar um identificador de entrada de curto prazo do segundo tipo examinando seu membro **abFlags** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="78955-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="78955-117">Alguns provedores de serviços desmarcam um ou mais sinalizadores para criar identificadores de entrada de curto prazo com mais validade.</span><span class="sxs-lookup"><span data-stu-id="78955-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="78955-118">Por exemplo, os seguintes membros **abFlags** representam identificadores de entrada de curto prazo que podem ser usados por vários dias ou para várias sessões:</span><span class="sxs-lookup"><span data-stu-id="78955-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="78955-119">Os clientes adquirem, usem e descartam rapidamente identificadores de entrada de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="78955-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="78955-120">Para a maioria das partes, elas podem ser usadas da mesma maneira que os identificadores de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="78955-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="78955-121">Eles podem ser recuperados de uma tabela, passados para o método **OpenEntry** e comparados com o método **CompareEntryIDs** .</span><span class="sxs-lookup"><span data-stu-id="78955-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="78955-122">A única exceção é que eles nunca são retornados do método [IMAPIProp::](imapiprop-getprops.md) GetProps.</span><span class="sxs-lookup"><span data-stu-id="78955-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="78955-123">As propriedades retornadas \*\*\*\* de GetProps são sempre identificadores de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="78955-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78955-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="78955-124">See also</span></span>

- [<span data-ttu-id="78955-125">Identificadores de entrada MAPI</span><span class="sxs-lookup"><span data-stu-id="78955-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

