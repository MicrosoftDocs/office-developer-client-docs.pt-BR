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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342137"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="3ed4e-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="3ed4e-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="3ed4e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ed4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ed4e-105">Mantém um servidor de formulário aberto na memória.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="3ed4e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ed4e-106">Parameters</span></span>

 <span data-ttu-id="3ed4e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ed4e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3ed4e-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3ed4e-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="3ed4e-109">_fLockServer_</span></span>
  
> <span data-ttu-id="3ed4e-110">[in] **true** para incrementar a contagem de bloqueio; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ed4e-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3ed4e-111">Return value</span></span>

<span data-ttu-id="3ed4e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ed4e-112">S_OK</span></span> 
  
> <span data-ttu-id="3ed4e-113">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ed4e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ed4e-114">Remarks</span></span>

<span data-ttu-id="3ed4e-115">Visualizadores de formulário chamam o **método IMAPIFormFactory::LockServer** para manter um aplicativo de servidor de formulário aberto na memória.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="3ed4e-116">Manter o servidor de formulários na memória melhora seu desempenho quando os formulários são criados e liberados com frequência.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3ed4e-117">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="3ed4e-117">Notes to implementers</span></span>

<span data-ttu-id="3ed4e-118">O **método IMAPIFormFactory::LockServer** é muito semelhante ao [método IClassFactory::LockServer.](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="3ed4e-119">Essencialmente, o **método IMAPIFormFactory::LockServer** mantém uma contagem de quantas vezes ele foi chamado; desde que essa contagem seja maior que 0, o método impede que o servidor de formulário seja descarregado da memória.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="3ed4e-120">Você pode usar a [função CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) para implementar isso.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-120">You can use the [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ed4e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ed4e-121">See also</span></span>



[<span data-ttu-id="3ed4e-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ed4e-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

