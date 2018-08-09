---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f6566f567c228b6416a64dbd58653561bb592e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767663"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="f3b42-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="f3b42-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="f3b42-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3b42-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3b42-105">Fornece um objeto de repositório IMAP Internet Message Access Protocol () que foi desfeita e que permite o acesso aos itens no arquivo de pastas particulares (. PST) sem sincronização de invocação e baixando os itens.</span><span class="sxs-lookup"><span data-stu-id="f3b42-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f3b42-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="f3b42-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3b42-107">Herdado de:</span><span class="sxs-lookup"><span data-stu-id="f3b42-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="f3b42-108">IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3b42-108">IUnknown</span></span>](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="f3b42-109">Fornecido por:</span><span class="sxs-lookup"><span data-stu-id="f3b42-109">Provided By:</span></span>  <br/> |<span data-ttu-id="f3b42-110">Provedor de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="f3b42-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="f3b42-111">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="f3b42-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f3b42-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="f3b42-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f3b42-113">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="f3b42-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="f3b42-114">*Membro do espaço reservado*</span><span class="sxs-lookup"><span data-stu-id="f3b42-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="f3b42-115">*Não tem suporte ou documentadas.*</span><span class="sxs-lookup"><span data-stu-id="f3b42-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="f3b42-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="f3b42-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="f3b42-117">Obtém um ponteiro para um repositório IMAP desfeito.</span><span class="sxs-lookup"><span data-stu-id="f3b42-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="f3b42-118">*Membro do espaço reservado*</span><span class="sxs-lookup"><span data-stu-id="f3b42-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="f3b42-119">*Não tem suporte ou documentadas.*</span><span class="sxs-lookup"><span data-stu-id="f3b42-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3b42-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3b42-120">Remarks</span></span>

<span data-ttu-id="f3b42-121">Chame [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) no armazenamento da mensagem de origem para obter a interface **IProxyStoreObject** .</span><span class="sxs-lookup"><span data-stu-id="f3b42-121">Call [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="f3b42-122">Em seguida, chame **IProxyStoreObject::UnwrapNoRef** para obter o objeto store desfeita.</span><span class="sxs-lookup"><span data-stu-id="f3b42-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="f3b42-123">Se **QueryInterface** retornará o erro **MAPI_E_INTERFACE_NOT_SUPPORTED**, em seguida, o repositório não foi quebrado.</span><span class="sxs-lookup"><span data-stu-id="f3b42-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="f3b42-124">Porque **UnwrapNoRef** não incrementa a contagem de referência para este novo ponteiro para o objeto de repositório desfeita, após chamar o **UnwrapNoRef**com êxito, você deve chamar [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) para manter a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="f3b42-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

