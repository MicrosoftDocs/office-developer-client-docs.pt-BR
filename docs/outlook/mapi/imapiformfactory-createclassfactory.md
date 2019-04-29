---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416073"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="4f1c1-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="4f1c1-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="4f1c1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f1c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f1c1-105">Retorna um objeto Factory de classe para o formulário.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="4f1c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f1c1-106">Parameters</span></span>

 <span data-ttu-id="4f1c1-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="4f1c1-107">_clsidForm_</span></span>
  
> <span data-ttu-id="4f1c1-108">no Um identificador de classe para o formulário a ser criado pela fábrica de classes.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="4f1c1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f1c1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4f1c1-110">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4f1c1-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="4f1c1-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="4f1c1-112">bota Um ponteiro para o objeto Factory de classe.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f1c1-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4f1c1-113">Return value</span></span>

<span data-ttu-id="4f1c1-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f1c1-114">S_OK</span></span> 
  
> <span data-ttu-id="4f1c1-115">O objeto Factory de classe foi retornado.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f1c1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f1c1-116">Remarks</span></span>

<span data-ttu-id="4f1c1-117">Os visualizadores de formulários chamam o método **IMAPIFormFactory:: CreateClassFactory** para obter um alocador de classe para um formulário específico.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="4f1c1-118">A fábrica de classes é usada para criar instâncias de um formulário que manipula mensagens de uma classe específica e para controlar o acesso a essas instâncias.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="4f1c1-119">O método **CreateClassFactory** é chamado por visualizadores de formulários para obter um objeto Factory de classe para servidores de formulário que implementam várias classes de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="4f1c1-120">Este método recebe um identificador de classe (CLSID) como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="4f1c1-121">Com base nesse parâmetro, este método pode determinar o tipo de objeto de fábrica de classe específico a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4f1c1-122">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="4f1c1-122">Notes to implementers</span></span>

<span data-ttu-id="4f1c1-123">Você pode retornar da implementação do **CreateClassFactory** o mesmo objeto de fábrica de classe em várias chamadas para o mesmo identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="4f1c1-124">Não é necessário criar uma nova instância de fábrica de classes.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="4f1c1-125">Você pode ter uma implementação de fábrica de classe única que cria instâncias de fábrica de classe apropriadas sob demanda ou várias implementações de fábrica de classes, uma para cada classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4f1c1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f1c1-126">See also</span></span>



[<span data-ttu-id="4f1c1-127">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f1c1-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

