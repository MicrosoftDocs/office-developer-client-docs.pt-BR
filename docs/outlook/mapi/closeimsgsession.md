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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412034"
---
# <a name="closeimsgsession"></a><span data-ttu-id="5450b-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="5450b-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="5450b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5450b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5450b-105">Fecha uma sessão de mensagem e todas as mensagens criadas nessa sessão.</span><span class="sxs-lookup"><span data-stu-id="5450b-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5450b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5450b-106">Header file:</span></span>  <br/> |<span data-ttu-id="5450b-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="5450b-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="5450b-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5450b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5450b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5450b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5450b-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="5450b-110">Called by:</span></span>  <br/> |<span data-ttu-id="5450b-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="5450b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="5450b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5450b-112">Parameters</span></span>

 <span data-ttu-id="5450b-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="5450b-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="5450b-114">no Ponteiro para o objeto de sessão de mensagem obtido usando a função [OpenIMsgSession](openimsgsession.md) no início da sessão de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5450b-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5450b-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5450b-115">Return value</span></span>

<span data-ttu-id="5450b-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5450b-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5450b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5450b-117">Remarks</span></span>

<span data-ttu-id="5450b-118">Uma sessão de mensagem é usada por aplicativos cliente e provedores de serviços que desejam lidar com vários objetos MAPI **IMessage** relacionados criados na parte superior dos objetos OLE **IStorage** subjacentes.</span><span class="sxs-lookup"><span data-stu-id="5450b-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="5450b-119">O cliente ou provedor usa as funções [OpenIMsgSession](openimsgsession.md) e **CloseIMsgSession** para quebrar a criação dessas mensagens dentro de uma sessão de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5450b-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="5450b-120">Depois que a sessão de mensagem é aberta, o cliente ou o provedor passa um ponteiro para ele em uma chamada para [OpenIMsgOnIStg](openimsgonistg.md) para criar um novo objeto **IMessage**-on- **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="5450b-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="5450b-121">Uma sessão de mensagem mantém o controle de todos os objetos **IMessage**-on- **IStorage** abertos durante a duração da sessão, além de todos os anexos e outras propriedades das mensagens.</span><span class="sxs-lookup"><span data-stu-id="5450b-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="5450b-122">Quando um cliente ou provedor chama **CloseIMsgSession**, ele fecha todos esses objetos.</span><span class="sxs-lookup"><span data-stu-id="5450b-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="5450b-123">Chamar **CloseIMsgSession** é a única maneira de fechar os objetos **IMessage**-on- **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="5450b-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

