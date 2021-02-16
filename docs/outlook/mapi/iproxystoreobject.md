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
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315516"
---
# <a name="iproxystoreobject"></a><span data-ttu-id="2c210-103">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="2c210-103">IProxyStoreObject</span></span>

  
  
<span data-ttu-id="2c210-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c210-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c210-105">Fornece um objeto de armazenamento IMAP (Internet Message Access Protocol) que foi deswrapped e que permite o acesso a itens no arquivo de Pastas Particulares (PST) sem invocar a sincronização e baixar os itens.</span><span class="sxs-lookup"><span data-stu-id="2c210-105">Provides an Internet Message Access Protocol (IMAP) store object that has been unwrapped and that allows access to items in the Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2c210-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2c210-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c210-107">Herdado de:</span><span class="sxs-lookup"><span data-stu-id="2c210-107">Inherited from:</span></span>  <br/> |[<span data-ttu-id="2c210-108">IUnknown</span><span class="sxs-lookup"><span data-stu-id="2c210-108">IUnknown</span></span>](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|<span data-ttu-id="2c210-109">Fornecido por:</span><span class="sxs-lookup"><span data-stu-id="2c210-109">Provided By:</span></span>  <br/> |<span data-ttu-id="2c210-110">Provedor de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="2c210-110">Message store provider</span></span>  <br/> |
|<span data-ttu-id="2c210-111">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="2c210-111">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2c210-112">**IID_IProxyStoreObject**</span><span class="sxs-lookup"><span data-stu-id="2c210-112">**IID_IProxyStoreObject**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2c210-113">Vtable order</span><span class="sxs-lookup"><span data-stu-id="2c210-113">Vtable order</span></span>

|||
|:-----|:-----|
| <span data-ttu-id="2c210-114">*Membro placeholder*</span><span class="sxs-lookup"><span data-stu-id="2c210-114">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="2c210-115">*Sem suporte ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="2c210-115">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="2c210-116">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="2c210-116">IProxyStoreObject::UnwrapNoRef</span></span>](iproxystoreobject-unwrapnoref.md) <br/> |<span data-ttu-id="2c210-117">Obtém um ponteiro para um armazenamento IMAP não mapeado.</span><span class="sxs-lookup"><span data-stu-id="2c210-117">Gets a pointer to an unwrapped IMAP store.</span></span>  <br/> |
| <span data-ttu-id="2c210-118">*Membro placeholder*</span><span class="sxs-lookup"><span data-stu-id="2c210-118">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="2c210-119">*Sem suporte ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="2c210-119">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c210-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c210-120">Remarks</span></span>

<span data-ttu-id="2c210-121">Chame [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) no repositório de mensagens de origem para obter a interface **IProxyStoreObject.**</span><span class="sxs-lookup"><span data-stu-id="2c210-121">Call [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) on the source message store to obtain the **IProxyStoreObject** interface.</span></span> <span data-ttu-id="2c210-122">Em seguida, **chame IProxyStoreObject::UnwrapNoRef** para obter o objeto de repositório não mapeado.</span><span class="sxs-lookup"><span data-stu-id="2c210-122">Then call **IProxyStoreObject::UnwrapNoRef** to obtain the unwrapped store object.</span></span> <span data-ttu-id="2c210-123">Se **QueryInterface** retornar o erro **MAPI_E_INTERFACE_NOT_SUPPORTED**, o armazenamento não foi empacotado.</span><span class="sxs-lookup"><span data-stu-id="2c210-123">If **QueryInterface** returns the error **MAPI_E_INTERFACE_NOT_SUPPORTED**, then the store has not been wrapped.</span></span> 
  
<span data-ttu-id="2c210-124">Como **UnwrapNoRef** não incrementa a contagem de referência desse novo ponteiro para o objeto de armazenamento não mapeado, depois de chamar **UnwrapNoRef** com êxito, você deve chamar [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) para manter a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="2c210-124">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  

