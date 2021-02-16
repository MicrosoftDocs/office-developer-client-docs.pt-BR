---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320150"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="c6680-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="c6680-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="c6680-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6680-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6680-105">Obtém um ponteiro para um objeto de armazenamento IMAP (Internet Message Access Protocol) não mapeado que fornece acesso ao arquivo de Pastas Particulares (PST) subjacente sem invocar a sincronização e baixar os itens.</span><span class="sxs-lookup"><span data-stu-id="c6680-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="c6680-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6680-106">Parameters</span></span>

 <span data-ttu-id="c6680-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="c6680-107">_ppvObject_</span></span>
  
> <span data-ttu-id="c6680-108">[out] Ponteiro para um [IMsgStore : objeto de repositório IMAPIProp](imsgstoreimapiprop.md) que não está mapeado.</span><span class="sxs-lookup"><span data-stu-id="c6680-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="c6680-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c6680-109">Return values</span></span>

<span data-ttu-id="c6680-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6680-110">S_OK</span></span>
  
- <span data-ttu-id="c6680-111">A chamada foi bem-sucedida e um ponteiro para uma interface não mapeada foi retornado em  _ppvObject_.</span><span class="sxs-lookup"><span data-stu-id="c6680-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6680-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6680-112">Remarks</span></span>

<span data-ttu-id="c6680-113">Sem primeiro desempacar um armazenamento IMAP, acessar uma mensagem no armazenamento pode forçar uma sincronização que tenta baixar a mensagem inteira.</span><span class="sxs-lookup"><span data-stu-id="c6680-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="c6680-114">O uso do armazenamento não mapeado permite o acesso à mensagem em seu estado atual sem acionar um download.</span><span class="sxs-lookup"><span data-stu-id="c6680-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="c6680-115">Como **UnwrapNoRef** não incrementa a contagem de referência desse novo ponteiro para o objeto de armazenamento não mapeado, depois de chamar **UnwrapNoRef** com êxito, você deve chamar [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para manter a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="c6680-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6680-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6680-116">See also</span></span>



[<span data-ttu-id="c6680-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="c6680-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

