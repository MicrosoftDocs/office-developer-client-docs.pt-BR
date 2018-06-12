---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c190691c8cfcb9b049bcf9ee4f21436e20955def
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766282"
---
# <a name="closeimsgsession"></a><span data-ttu-id="40ae1-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="40ae1-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="40ae1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="40ae1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="40ae1-105">Fecha uma sessão de mensagem e todas as mensagens criadas dentro dessa sessão.</span><span class="sxs-lookup"><span data-stu-id="40ae1-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40ae1-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="40ae1-106">Header file:</span></span>  <br/> |<span data-ttu-id="40ae1-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="40ae1-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="40ae1-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="40ae1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="40ae1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="40ae1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="40ae1-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="40ae1-110">Called by:</span></span>  <br/> |<span data-ttu-id="40ae1-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="40ae1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="40ae1-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="40ae1-112">Parameters</span></span>

 <span data-ttu-id="40ae1-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="40ae1-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="40ae1-114">[in] Ponteiro para o objeto de sessão de mensagem obtido com a função [OpenIMsgSession](openimsgsession.md) no início da sessão de mensagem.</span><span class="sxs-lookup"><span data-stu-id="40ae1-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="40ae1-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="40ae1-115">Return value</span></span>

<span data-ttu-id="40ae1-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="40ae1-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40ae1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="40ae1-117">Remarks</span></span>

<span data-ttu-id="40ae1-118">Uma sessão de mensagens é usada por aplicativos cliente e provedores de serviços que deseja lidar com vários objetos relacionados de MAPI **IMessage** construídos sobre objetos OLE **IStorage** subjacentes.</span><span class="sxs-lookup"><span data-stu-id="40ae1-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="40ae1-119">O cliente ou o provedor usa as funções [OpenIMsgSession](openimsgsession.md) e **CloseIMsgSession** para quebrar a criação dessas mensagens de uma sessão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="40ae1-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="40ae1-120">Depois que a sessão de mensagens é aberta, o cliente ou o provedor passa um ponteiro para ele em uma chamada para [OpenIMsgOnIStg](openimsgonistg.md) para criar um novo **IMessage**- on - objeto **|** .</span><span class="sxs-lookup"><span data-stu-id="40ae1-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="40ae1-121">Uma sessão de mensagens rastreia de todos os objetos de **IMessage**- on - **IStorage** abertos durante a duração da sessão, além de todos os anexos e outras propriedades das mensagens.</span><span class="sxs-lookup"><span data-stu-id="40ae1-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="40ae1-122">Quando um cliente ou provedor chama **CloseIMsgSession**, ele fecha todos esses objetos.</span><span class="sxs-lookup"><span data-stu-id="40ae1-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="40ae1-123">Chamar o **CloseIMsgSession** é a única maneira de fechar **IMessage**- on - **IStorage** objetos.</span><span class="sxs-lookup"><span data-stu-id="40ae1-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

