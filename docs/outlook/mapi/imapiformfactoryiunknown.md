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
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342116"
---
# <a name="imapiformfactory--iunknown"></a><span data-ttu-id="d20ad-103">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d20ad-103">IMAPIFormFactory : IUnknown</span></span>

  
  
<span data-ttu-id="d20ad-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d20ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d20ad-105">Oferece suporte ao uso de formulários de tempo de executar configuráveis em ambientes de computação distribuída.</span><span class="sxs-lookup"><span data-stu-id="d20ad-105">Supports the use of configurable run-time forms in distributed computing environments.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d20ad-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d20ad-106">Header file:</span></span>  <br/> |<span data-ttu-id="d20ad-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="d20ad-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="d20ad-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="d20ad-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="d20ad-109">Objetos de fábrica de formulário</span><span class="sxs-lookup"><span data-stu-id="d20ad-109">Form factory objects</span></span>  <br/> |
|<span data-ttu-id="d20ad-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d20ad-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="d20ad-111">Servidores de formulário</span><span class="sxs-lookup"><span data-stu-id="d20ad-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="d20ad-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="d20ad-112">Called by:</span></span>  <br/> |<span data-ttu-id="d20ad-113">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="d20ad-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="d20ad-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="d20ad-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d20ad-115">IID_IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="d20ad-115">IID_IMAPIFormFactory</span></span>  <br/> |
|<span data-ttu-id="d20ad-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="d20ad-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="d20ad-117">LPMAPIFORMFACTORY</span><span class="sxs-lookup"><span data-stu-id="d20ad-117">LPMAPIFORMFACTORY</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d20ad-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="d20ad-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d20ad-119">CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="d20ad-119">CreateClassFactory</span></span>](imapiformfactory-createclassfactory.md) <br/> |<span data-ttu-id="d20ad-120">Retorna um objeto de fábrica de classe para o formulário.</span><span class="sxs-lookup"><span data-stu-id="d20ad-120">Returns a class factory object for the form.</span></span>  <br/> |
|[<span data-ttu-id="d20ad-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="d20ad-121">GetLastError</span></span>](imapiformfactory-getlasterror.md) <br/> |<span data-ttu-id="d20ad-122">Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior ocorrendo no objeto de fábrica de formulário.</span><span class="sxs-lookup"><span data-stu-id="d20ad-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form factory object.</span></span>  <br/> |
|[<span data-ttu-id="d20ad-123">LockServer</span><span class="sxs-lookup"><span data-stu-id="d20ad-123">LockServer</span></span>](imapiformfactory-lockserver.md) <br/> |<span data-ttu-id="d20ad-124">Mantém um servidor de formulário aberto na memória.</span><span class="sxs-lookup"><span data-stu-id="d20ad-124">Keeps an open form server in memory.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d20ad-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="d20ad-125">Remarks</span></span>

<span data-ttu-id="d20ad-126">A interface **IMAPIFormFactory** é baseada na interface [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) e os objetos que implementam **IMAPIFormFactory** também devem herdar **de IClassFactory**.</span><span class="sxs-lookup"><span data-stu-id="d20ad-126">The **IMAPIFormFactory** interface is based on the [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) interface, and objects that implement **IMAPIFormFactory** should also inherit from **IClassFactory**.</span></span>
  
 <span data-ttu-id="d20ad-127">**IMAPIFormFactory** é a interface que os visualizadores de formulário usam para criar novos objetos de formulário quando um servidor de formulário oferece suporte a mais de uma classe de mensagem (ou seja, mais de um tipo de objeto de formulário).</span><span class="sxs-lookup"><span data-stu-id="d20ad-127">**IMAPIFormFactory** is the interface that form viewers use to create new form objects when a form server supports more than one message class (that is, more than one type of form object).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d20ad-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d20ad-128">See also</span></span>



[<span data-ttu-id="d20ad-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="d20ad-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

