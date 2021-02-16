---
title: Convenção de Nomen por Valor de Retorno
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423612"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="26808-103">Convenção de Nomen por Valor de Retorno</span><span class="sxs-lookup"><span data-stu-id="26808-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="26808-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26808-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26808-105">O MAPICODE. O arquivo de header H contém muitos dos valores que um cliente ou provedor de serviços pode retornar de uma implementação de método de interface ou pode ver retornado de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="26808-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="26808-106">Os códigos para representar condições de aviso e falha seguem uma convenção de nomenal diferente que começa com o prefixo MAPI, um sublinhado e um W ou E para indicar o tipo de código.</span><span class="sxs-lookup"><span data-stu-id="26808-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="26808-107">O restante do código é uma cadeia de caracteres curta para descrever a condição.</span><span class="sxs-lookup"><span data-stu-id="26808-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="26808-108">Cada palavra na cadeia de caracteres é separada por um sublinhado.</span><span class="sxs-lookup"><span data-stu-id="26808-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="26808-109">Por exemplo, o valor de MAPI_E_TOO_COMPLEX indica que a implementação não pôde manipular o que estava sendo solicitado na chamada.</span><span class="sxs-lookup"><span data-stu-id="26808-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="26808-110">O valor de MAPI_W_PARTIAL_COMPLETION indica que a chamada foi bem-sucedida, mas que houve problemas.</span><span class="sxs-lookup"><span data-stu-id="26808-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="26808-111">Somente parte da operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="26808-111">Only part of the operation was completed successfully.</span></span>
  

