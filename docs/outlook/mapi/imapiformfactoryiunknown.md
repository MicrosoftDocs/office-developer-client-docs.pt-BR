---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 651ef6a7c1af70c75a85e13414c4fd7632d30290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767038"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="0b232-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b232-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="0b232-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b232-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0b232-105">Suporta o uso dos formulários configuráveis de tempo de execução em ambientes de computação distribuídos.</span><span class="sxs-lookup"><span data-stu-id="0b232-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b232-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0b232-106">Header file:</span></span>  <br/> |<span data-ttu-id="0b232-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="0b232-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="0b232-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="0b232-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0b232-109">Objetos de fábrica do formulário</span><span class="sxs-lookup"><span data-stu-id="0b232-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="0b232-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0b232-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0b232-111">Servidores de formulário</span><span class="sxs-lookup"><span data-stu-id="0b232-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="0b232-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0b232-112">Called by:</span></span>  <br/> |<span data-ttu-id="0b232-113">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="0b232-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="0b232-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="0b232-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0b232-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="0b232-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="0b232-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="0b232-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0b232-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="0b232-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0b232-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="0b232-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0b232-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="0b232-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="0b232-120">Retorna um objeto de fábrica de classe do formulário.</span><span class="sxs-lookup"><span data-stu-id="0b232-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="0b232-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="0b232-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="0b232-122">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorrem ao objeto form fábrica.</span><span class="sxs-lookup"><span data-stu-id="0b232-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="0b232-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="0b232-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="0b232-124">Mantém um servidor de formulário aberto na memória.</span><span class="sxs-lookup"><span data-stu-id="0b232-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b232-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b232-125">Remarks</span></span>

<span data-ttu-id="0b232-126">A interface **IMAPIFormFactory** baseia-se na interface [IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) e objetos que implementam **IMAPIFormFactory** também devem herdar de **IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="0b232-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="0b232-127">**IMAPIFormFactory** é a interface que os visualizadores de formulário usam para criar novos objetos de formulário quando um servidor de formulário oferece suporte a mais de uma classe de mensagem (ou seja, mais de um tipo de objeto do formulário).</span><span class="sxs-lookup"><span data-stu-id="0b232-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b232-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b232-128">See also</span></span>



[<span data-ttu-id="0b232-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="0b232-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

