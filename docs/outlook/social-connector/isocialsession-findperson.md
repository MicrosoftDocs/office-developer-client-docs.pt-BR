---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtém uma cadeia de caracteres que representa uma ou mais pessoas que correspondem ao parâmetro userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434792"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="afb7b-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="afb7b-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="afb7b-104">Obtém uma cadeia de caracteres que representa uma ou mais pessoas que correspondem ao parâmetro _userid_ .</span><span class="sxs-lookup"><span data-stu-id="afb7b-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="afb7b-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afb7b-105">Parameters</span></span>

<span data-ttu-id="afb7b-106">_ID_</span><span class="sxs-lookup"><span data-stu-id="afb7b-106">_userId_</span></span>
  
> <span data-ttu-id="afb7b-107">no Uma ID de usuário de rede social, um endereço SMTP ou um nome de exibição de uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="afb7b-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="afb7b-108">_result_</span><span class="sxs-lookup"><span data-stu-id="afb7b-108">_result_</span></span>
  
> <span data-ttu-id="afb7b-109">bota Uma sequência de caracteres XML que representa uma ou mais pessoas que correspondem às informações de identificação especificadas pelo parâmetro _userid_ .</span><span class="sxs-lookup"><span data-stu-id="afb7b-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="afb7b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="afb7b-110">Remarks</span></span>

<span data-ttu-id="afb7b-111">Se uma ou mais pessoas corresponderem à solicitação **FindPerson** , este método retornará as informações dessas pessoas no parâmetro _Result_ .</span><span class="sxs-lookup"><span data-stu-id="afb7b-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="afb7b-112">A cadeia de caracteres XML do _resultado_ deve estar em conformidade com a definição de esquema para **amigos**, conforme definido no esquema para a extensibilidade do provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="afb7b-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="afb7b-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="afb7b-113">See also</span></span>

- [<span data-ttu-id="afb7b-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="afb7b-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

