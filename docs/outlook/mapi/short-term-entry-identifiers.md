---
title: Identificadores de entrada de curto prazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f601971e61eb6430bef9d50b093642ee04b14044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770403"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="bacc9-103">Identificadores de entrada de curto prazo</span><span class="sxs-lookup"><span data-stu-id="bacc9-103">Short-term entry identifiers</span></span>

<span data-ttu-id="bacc9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bacc9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bacc9-105">Um identificador de entrada de curto prazo é atribuído por um provedor de serviço a um objeto quando o identificador deve ser construído rapidamente e não precisa dure sobre tempo ou distância.</span><span class="sxs-lookup"><span data-stu-id="bacc9-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="bacc9-106">A exclusividade de um identificador de entrada de curto prazo é garantida somente durante a vigência da sessão atual na estação de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="bacc9-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="bacc9-107">Normalmente, um identificador de entrada de curto prazo é válido somente até que o objeto que ele representa for lançado.</span><span class="sxs-lookup"><span data-stu-id="bacc9-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="bacc9-108">Identificadores de entrada de curto prazo são atribuídos às linhas em tabelas e às entradas nas caixas de diálogo, onde é necessário fornecer dados rapidamente para navegação.</span><span class="sxs-lookup"><span data-stu-id="bacc9-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="bacc9-109">Por exemplo, provedores de armazenamento de mensagem atribuir identificadores de entrada de curto prazo às linhas de mensagens em uma tabela de conteúdo e para destinatários em uma tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="bacc9-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="bacc9-110">Clientes podem usar esses identificadores de entrada de curto prazo para abrir os objetos representados por linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="bacc9-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="bacc9-111">No entanto, ao contrário de longo prazo identificadores de entrada que podem ser usados com qualquer um dos métodos **OpenEntry** , a curto prazo identificadores de entrada devem ser usados com o método de **OpenEntry** do contêiner.</span><span class="sxs-lookup"><span data-stu-id="bacc9-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="bacc9-112">Implementando a curto prazo identificadores de entrada</span><span class="sxs-lookup"><span data-stu-id="bacc9-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="bacc9-113">Maneiras de implementar a curto prazo identificadores de entrada mais comuns incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="bacc9-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="bacc9-114">Os identificadores de entrada de curto prazo fazendo o mesmo que os identificadores de longo prazo, deixando todos os sinalizadores não definidas.</span><span class="sxs-lookup"><span data-stu-id="bacc9-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="bacc9-115">Tornando os identificadores de entrada de curto prazo diferente dos identificadores de longo prazo, a definição de todos os sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="bacc9-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="bacc9-116">Os clientes podem identificar um identificador de entrada de curto prazo do segundo tipo examinando sua lista de membros **abFlags** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="bacc9-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="bacc9-117">Alguns provedores de serviços desmarque um ou mais sinalizadores para criar a curto prazo identificadores de entrada que têm validade maior.</span><span class="sxs-lookup"><span data-stu-id="bacc9-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="bacc9-118">Por exemplo, os seguintes membros **abFlags** representam a curto prazo identificadores de entrada que podem ser usados para vários dias ou para várias sessões:</span><span class="sxs-lookup"><span data-stu-id="bacc9-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="bacc9-119">Clientes rapidamente adquirem, usam e descartar os identificadores de entrada de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="bacc9-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="bacc9-120">Na maioria das vezes, pode ser usados da mesma maneira como os identificadores de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="bacc9-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="bacc9-121">Eles podem ser recuperados de uma tabela, passadas para o método **OpenEntry** e comparado com o método **CompareEntryIDs** .</span><span class="sxs-lookup"><span data-stu-id="bacc9-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="bacc9-122">A única exceção é que nunca são retornadas pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="bacc9-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="bacc9-123">As propriedades retornadas de **GetProps** são sempre identificadores de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="bacc9-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bacc9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="bacc9-124">See also</span></span>

- [<span data-ttu-id="bacc9-125">Identificadores de entrada MAPI</span><span class="sxs-lookup"><span data-stu-id="bacc9-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

