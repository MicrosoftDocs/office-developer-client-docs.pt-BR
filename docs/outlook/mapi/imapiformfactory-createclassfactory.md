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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 823e10a1f496f5f5e8bab00f94d700d06e753b48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767039"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="cd539-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="cd539-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="cd539-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cd539-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cd539-105">Retorna um objeto de fábrica de classe do formulário.</span><span class="sxs-lookup"><span data-stu-id="cd539-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="cd539-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="cd539-106">Parameters</span></span>

 <span data-ttu-id="cd539-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="cd539-107">_clsidForm_</span></span>
  
> <span data-ttu-id="cd539-108">[in] Um identificador de classe do formulário a ser criado pela fábrica de classe.</span><span class="sxs-lookup"><span data-stu-id="cd539-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="cd539-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cd539-109">_ulFlags_</span></span>
  
> <span data-ttu-id="cd539-110">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cd539-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cd539-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="cd539-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="cd539-112">[out] Um ponteiro para o objeto de classe de fábrica.</span><span class="sxs-lookup"><span data-stu-id="cd539-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cd539-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="cd539-113">Return value</span></span>

<span data-ttu-id="cd539-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd539-114">S_OK</span></span> 
  
> <span data-ttu-id="cd539-115">O objeto de classe de fábrica foi retornado.</span><span class="sxs-lookup"><span data-stu-id="cd539-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd539-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="cd539-116">Remarks</span></span>

<span data-ttu-id="cd539-117">Visualizadores de formulário chame o método de **IMAPIFormFactory::CreateClassFactory** para obter um alocador de classe de um formulário específico.</span><span class="sxs-lookup"><span data-stu-id="cd539-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="cd539-118">O alocador de classe é usado para criar instâncias de um formulário que processa mensagens de uma classe específica e controlar o acesso a essas instâncias.</span><span class="sxs-lookup"><span data-stu-id="cd539-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="cd539-119">O método **CreateClassFactory** é chamado pelo visualizadores de formulário para obter um objeto de fábrica de classe para servidores de formulário que implementar várias classes de mensagem.</span><span class="sxs-lookup"><span data-stu-id="cd539-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="cd539-120">Esse método recebe um identificador de classe (CLSID) como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cd539-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="cd539-121">Com base no parâmetro, esse método pode determinar o tipo específico de objeto de fábrica de classe para retornar.</span><span class="sxs-lookup"><span data-stu-id="cd539-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cd539-122">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="cd539-122">Notes to implementers</span></span>

<span data-ttu-id="cd539-123">Você pode retornar da sua implementação **CreateClassFactory** o mesmo objeto de fábrica de classe em várias chamadas para o mesmo identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="cd539-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="cd539-124">Criando uma nova instância de fábrica de classe não é necessária.</span><span class="sxs-lookup"><span data-stu-id="cd539-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="cd539-125">Você pode ter uma implementação de fábrica de classe única que cria instâncias de fábrica de classe apropriado sob demanda ou várias implementações de fábrica de classe, uma para cada classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="cd539-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cd539-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd539-126">See also</span></span>



[<span data-ttu-id="cd539-127">IMAPIFormFactory: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd539-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

