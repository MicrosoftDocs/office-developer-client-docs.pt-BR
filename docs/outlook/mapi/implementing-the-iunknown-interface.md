---
title: Implementar a interface IUnknown
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
# <a name="implementing-the-iunknown-interface"></a><span data-ttu-id="5e0f7-103">Implementar a interface IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e0f7-103">Implementing the IUnknown Interface</span></span>

  
  
<span data-ttu-id="5e0f7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e0f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e0f7-105">Os métodos da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , implementados em todos os objetos MAPI, dão suporte ao gerenciamento de objeto e comunicação entre objetos.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-105">The methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface, implemented in every MAPI object, support interobject communication and object management.</span></span> 
  
 <span data-ttu-id="5e0f7-106">**IUnknown** tem três métodos: [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)e [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e0f7-106">**IUnknown** has three methods: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="5e0f7-107">**QueryInterface** habilita um objeto para determinar se outro objeto oferece suporte a uma interface específica.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-107">**QueryInterface** enables one object to determine whether another object supports a particular interface.</span></span> <span data-ttu-id="5e0f7-108">Com **QueryInterface**, dois objetos sem conhecimento prévio da funcionalidade de cada um podem interagir.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-108">With **QueryInterface**, two objects with no prior knowledge of each other's functionality can interact.</span></span> <span data-ttu-id="5e0f7-109">Se o objeto que implementa **QueryInterface** não oferecer suporte à interface em questão, ele retornará um ponteiro para a implementação da interface.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-109">If the object that implements **QueryInterface** does support the interface in question, it returns a pointer to the implementation of the interface.</span></span> <span data-ttu-id="5e0f7-110">Se o objeto não oferecer suporte à interface solicitada, ele retornará o valor MAPI_E_INTERFACE_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-110">If the object does not support the requested interface, it returns the MAPI_E_INTERFACE_NOT_SUPPORTED value.</span></span> 
  
<span data-ttu-id="5e0f7-111">Quando **QueryInterface** retorna um ponteiro de interface solicitado, ele também deve aumentar a contagem de referência do novo objeto.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-111">When **QueryInterface** returns a requested interface pointer, it must also increase the new object's reference count.</span></span> <span data-ttu-id="5e0f7-112">A contagem de referência de um objeto é um valor numérico usado para gerenciar o ciclo de vida do objeto.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-112">An object's reference count is a numeric value used to manage the object's lifespan.</span></span> <span data-ttu-id="5e0f7-113">Quando a contagem de referência é maior que 1, a memória do objeto não pode ser liberada porque está sendo usado ativamente.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-113">When the reference count is greater than 1, the object's memory cannot be freed because it is actively being used.</span></span> <span data-ttu-id="5e0f7-114">Só é quando a contagem de referência é descartada para 0 que o objeto pode ser liberado com segurança.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-114">It is only when the reference count drops to 0 that the object can be released safely.</span></span> 
  
<span data-ttu-id="5e0f7-115">Os outros dois métodos **IUnknown** , **AddRef** e **Release**, gerenciam a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-115">The other two **IUnknown** methods, **AddRef** and **Release**, manage the reference count.</span></span> <span data-ttu-id="5e0f7-116">**AddRef** incrementa a contagem de referência, enquanto a **versão** diminui.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-116">**AddRef** increments the reference count, while **Release** decrements it.</span></span> <span data-ttu-id="5e0f7-117">Todos os métodos ou funções de API que retornam ponteiros de interface, como **QueryInterface**, devem chamar **AddRef** para incrementar a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-117">All methods or API functions that return interface pointers, such as **QueryInterface**, must call **AddRef** to increment the reference count.</span></span> <span data-ttu-id="5e0f7-118">Todas as implementações de métodos que recebem ponteiros de interface devem chamar **Release** para decrementar a contagem quando o ponteiro não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-118">All implementations of methods that receive interface pointers must call **Release** to decrement the count when the pointer is no longer needed.</span></span> <span data-ttu-id="5e0f7-119">**Release** verifica se há uma contagem de referência existente, liberando a memória associada à interface somente se a contagem for 0.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-119">**Release** checks for an existing reference count, freeing the memory associated with the interface only if the count is 0.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5e0f7-120">Como **AddRef** e **Release** não são necessários para retornar valores precisos, os chamadores desses métodos não devem usar os valores de retorno para determinar se um objeto ainda é válido ou foi destruído.</span><span class="sxs-lookup"><span data-stu-id="5e0f7-120">Because **AddRef** and **Release** are not required to return accurate values, callers of these methods must not use the return values to determine whether an object is still valid or has been destroyed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e0f7-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e0f7-121">See also</span></span>



[<span data-ttu-id="5e0f7-122">Implementar objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="5e0f7-122">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

