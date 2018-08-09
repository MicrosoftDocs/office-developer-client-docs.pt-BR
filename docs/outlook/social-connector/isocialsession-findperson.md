---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtém um string que representa uma ou mais pessoas que coincidem com o parâmetro userID.
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770852"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="fefbc-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="fefbc-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="fefbc-104">Obtém um string que representa uma ou mais pessoas que coincidem com o parâmetro _userID_ .</span><span class="sxs-lookup"><span data-stu-id="fefbc-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="fefbc-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fefbc-105">Parameters</span></span>

<span data-ttu-id="fefbc-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="fefbc-106">_userId_</span></span>
  
> <span data-ttu-id="fefbc-107">[in] Uma ID de usuário de rede social, endereço SMTP ou nome de exibição de uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="fefbc-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="fefbc-108">_resultado_</span><span class="sxs-lookup"><span data-stu-id="fefbc-108">_result_</span></span>
  
> <span data-ttu-id="fefbc-109">[out] Uma sequência de caracteres XML que representa uma ou mais pessoas que coincidem com as informações de identificação especificadas pelo parâmetro _userId_ .</span><span class="sxs-lookup"><span data-stu-id="fefbc-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fefbc-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fefbc-110">Remarks</span></span>

<span data-ttu-id="fefbc-111">Se a solicitação de **FindPerson** corresponderem a uma ou mais pessoas, esse método retorna as informações de pessoas no parâmetro _resultado_ .</span><span class="sxs-lookup"><span data-stu-id="fefbc-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="fefbc-112">A cadeia de caracteres XML de _resultado_ deve estar em conformidade com a definição de esquema para **amigos**, conforme definido no esquema para fornecer extensibilidade de provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="fefbc-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fefbc-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="fefbc-113">See also</span></span>

- [<span data-ttu-id="fefbc-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fefbc-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

