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
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389050"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="71bf8-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="71bf8-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="71bf8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71bf8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71bf8-105">Mantém um servidor de formulário aberto na memória.</span><span class="sxs-lookup"><span data-stu-id="71bf8-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="71bf8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71bf8-106">Parameters</span></span>

 <span data-ttu-id="71bf8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="71bf8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="71bf8-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="71bf8-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="71bf8-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="71bf8-109">_fLockServer_</span></span>
  
> <span data-ttu-id="71bf8-110">[in] **true** para incrementar a contagem de bloqueio; Caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="71bf8-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="71bf8-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="71bf8-111">Return value</span></span>

<span data-ttu-id="71bf8-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="71bf8-112">S_OK</span></span> 
  
> <span data-ttu-id="71bf8-113">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="71bf8-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="71bf8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="71bf8-114">Remarks</span></span>

<span data-ttu-id="71bf8-115">Visualizadores de formulário chame o método de **IMAPIFormFactory::LockServer** para manter um aplicativo de servidor do formulário aberto na memória.</span><span class="sxs-lookup"><span data-stu-id="71bf8-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="71bf8-116">Manter o servidor de formulário na memória melhora o seu desempenho quando formulários frequentemente são criados e lançados.</span><span class="sxs-lookup"><span data-stu-id="71bf8-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="71bf8-117">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="71bf8-117">Notes to implementers</span></span>

<span data-ttu-id="71bf8-118">O método **IMAPIFormFactory::LockServer** é muito semelhante ao método [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="71bf8-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="71bf8-119">Basicamente, o método **IMAPIFormFactory::LockServer** mantém uma contagem de quantas vezes ele tiver sido chamada; desde que essa contagem for maior que 0, o método impede que o servidor do formulário está sendo descarregado da memória.</span><span class="sxs-lookup"><span data-stu-id="71bf8-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="71bf8-120">Você pode usar a função [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) para implementar isso.</span><span class="sxs-lookup"><span data-stu-id="71bf8-120">You can use the [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="71bf8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="71bf8-121">See also</span></span>



[<span data-ttu-id="71bf8-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="71bf8-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

