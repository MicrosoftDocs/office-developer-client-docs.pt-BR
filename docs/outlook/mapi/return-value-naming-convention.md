---
title: Valor de retorno convenção de nomenclatura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 990a48c661621a3a704236a850f5d09239a12fca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770275"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="7c77b-103">Valor de retorno convenção de nomenclatura</span><span class="sxs-lookup"><span data-stu-id="7c77b-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="7c77b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c77b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c77b-105">O MAPICODE. Arquivo de cabeçalho H contém muitos dos valores que um provedor de cliente ou serviço pode retornar de uma implementação do método de interface ou pode ver retornado de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="7c77b-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="7c77b-106">Os códigos para representar as condições de aviso e de falha siga uma convenção de nomenclatura diferente que começa com o prefixo MAPI, um caractere de sublinhado e um W ou um E para indicar o tipo de código.</span><span class="sxs-lookup"><span data-stu-id="7c77b-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="7c77b-107">O restante do código é uma cadeia de caracteres curta para descrever a condição.</span><span class="sxs-lookup"><span data-stu-id="7c77b-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="7c77b-108">Cada palavra na cadeia de caracteres é separada por um caractere de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="7c77b-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="7c77b-109">Por exemplo, o valor de erro MAPI_E_TOO_COMPLEX indica que a implementação não pôde tratar qualquer item estava sendo solicitado na chamada.</span><span class="sxs-lookup"><span data-stu-id="7c77b-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="7c77b-110">O valor de aviso MAPI_W_PARTIAL_COMPLETION indica que a chamada foi bem-sucedida, mas houve problemas.</span><span class="sxs-lookup"><span data-stu-id="7c77b-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="7c77b-111">Somente a parte da operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="7c77b-111">Only part of the operation was completed successfully.</span></span>
  

