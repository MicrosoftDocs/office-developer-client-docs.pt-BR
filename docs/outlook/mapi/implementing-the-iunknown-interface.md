---
title: Implementando a interface IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310042"
---
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="20f4d-103">Implementando a interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="20f4d-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="20f4d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20f4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20f4d-105">Os métodos da interface [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) implementados em cada objeto MAPI, suportam comunicação interobjeto e gerenciamento de objetos.</span><span class="sxs-lookup"><span data-stu-id="20f4d-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="20f4d-106">**IUnknown** tem três métodos: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)e [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="20f4d-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="20f4d-107">**QueryInterface** permite que um objeto determine se outro objeto oferece suporte a uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="20f4d-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="20f4d-108">Com **QueryInterface**, dois objetos sem conhecimento prévio sobre a funcionalidade uns dos outros podem interagir.</span><span class="sxs-lookup"><span data-stu-id="20f4d-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="20f4d-109">Se o objeto que implementa **QueryInterface** suporta a interface em questão, ele retorna um ponteiro para a implementação da interface.</span><span class="sxs-lookup"><span data-stu-id="20f4d-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="20f4d-110">Se o objeto não suportar a interface solicitada, ele retornará o MAPI_E_INTERFACE_NOT_SUPPORTED valor.</span><span class="sxs-lookup"><span data-stu-id="20f4d-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="20f4d-111">Quando **QueryInterface** retorna um ponteiro de interface solicitado, ele também deve aumentar a contagem de referência do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="20f4d-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="20f4d-112">A contagem de referência de um objeto é um valor numérico usado para gerenciar o tempo de vida do objeto.</span><span class="sxs-lookup"><span data-stu-id="20f4d-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="20f4d-113">Quando a contagem de referência é maior que 1, a memória do objeto não pode ser liberada porque está sendo usada ativamente.</span><span class="sxs-lookup"><span data-stu-id="20f4d-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="20f4d-114">É apenas quando a contagem de referência cai para 0 que o objeto pode ser liberado com segurança.</span><span class="sxs-lookup"><span data-stu-id="20f4d-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="20f4d-115">Os outros dois **métodos IUnknown,** **AddRef** e **Release,** gerenciam a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="20f4d-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="20f4d-116">**AddRef** incrementa a contagem de referência, enquanto **Release** a diminui.</span><span class="sxs-lookup"><span data-stu-id="20f4d-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="20f4d-117">Todos os métodos ou funções de API que retornam ponteiros de interface, como **QueryInterface,** devem chamar **AddRef** para incrementar a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="20f4d-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="20f4d-118">Todas as implementações de métodos que recebem ponteiros de interface devem chamar **Release** para rebaixar a contagem quando o ponteiro não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="20f4d-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="20f4d-119">**Verificações** de versão para uma contagem de referência existente, liberando a memória associada à interface somente se a contagem for 0.</span><span class="sxs-lookup"><span data-stu-id="20f4d-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="20f4d-120">Como **AddRef** e **Release** não são necessários para retornar valores precisos, os chamadores desses métodos não devem usar os valores de retorno para determinar se um objeto ainda é válido ou foi destruído.</span><span class="sxs-lookup"><span data-stu-id="20f4d-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20f4d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="20f4d-121">See also</span></span>



[<span data-ttu-id="20f4d-122">Implementando objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="20f4d-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

