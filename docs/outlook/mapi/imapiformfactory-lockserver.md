---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c33fea8a2aba875fcdc06dea3343add4b7ac5dde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767014"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="4a655-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="4a655-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="4a655-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a655-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a655-105">Mantém um servidor de formulário aberto na memória.</span><span class="sxs-lookup"><span data-stu-id="4a655-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="4a655-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4a655-106">Parameters</span></span>

 <span data-ttu-id="4a655-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4a655-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4a655-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4a655-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4a655-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="4a655-109">_fLockServer_</span></span>
  
> <span data-ttu-id="4a655-110">[in] **true** para incrementar a contagem de bloqueio; Caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="4a655-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4a655-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4a655-111">Return value</span></span>

<span data-ttu-id="4a655-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="4a655-112">S_OK</span></span> 
  
> <span data-ttu-id="4a655-113">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="4a655-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4a655-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="4a655-114">Remarks</span></span>

<span data-ttu-id="4a655-115">Visualizadores de formulário chame o método de **IMAPIFormFactory::LockServer** para manter um aplicativo de servidor do formulário aberto na memória.</span><span class="sxs-lookup"><span data-stu-id="4a655-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="4a655-116">Manter o servidor de formulário na memória melhora o seu desempenho quando formulários frequentemente são criados e lançados.</span><span class="sxs-lookup"><span data-stu-id="4a655-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4a655-117">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="4a655-117">Notes to implementers</span></span>

<span data-ttu-id="4a655-118">O método **IMAPIFormFactory::LockServer** é muito semelhante ao método [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4a655-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="4a655-119">Basicamente, o método **IMAPIFormFactory::LockServer** mantém uma contagem de quantas vezes ele tiver sido chamada; desde que essa contagem for maior que 0, o método impede que o servidor do formulário está sendo descarregado da memória.</span><span class="sxs-lookup"><span data-stu-id="4a655-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="4a655-120">Você pode usar a função [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx) para implementar isso.</span><span class="sxs-lookup"><span data-stu-id="4a655-120">You can use the [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4a655-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a655-121">See also</span></span>



[<span data-ttu-id="4a655-122">IMAPIFormFactory: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a655-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

