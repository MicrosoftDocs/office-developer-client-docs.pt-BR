---
title: Retornar convenção de nomenclatura de valor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4d7a95e4681370e1aaf4f8b4c4b7ca0814b3aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581843"
---
# <a name="return-value-naming-convention"></a><span data-ttu-id="dbe74-103">Retornar convenção de nomenclatura de valor</span><span class="sxs-lookup"><span data-stu-id="dbe74-103">Return Value Naming Convention</span></span>

  
  
<span data-ttu-id="dbe74-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbe74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbe74-105">O MAPICODE. Arquivo de cabeçalho H contém muitos dos valores que um provedor de cliente ou serviço pode retornar de uma implementação do método de interface ou pode ver retornado de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="dbe74-105">The MAPICODE.H header file contains many of the values that a client or service provider might return from an interface method implementation or might see returned from a call.</span></span>
  
<span data-ttu-id="dbe74-106">Os códigos para representar as condições de aviso e de falha siga uma convenção de nomenclatura diferente que começa com o prefixo MAPI, um caractere de sublinhado e um W ou um E para indicar o tipo de código.</span><span class="sxs-lookup"><span data-stu-id="dbe74-106">The codes to represent warning and failure conditions follow a different naming convention that begins with the prefix MAPI, an underscore, and either a W or an E to indicate the type of code.</span></span> <span data-ttu-id="dbe74-107">O restante do código é uma cadeia de caracteres curta para descrever a condição.</span><span class="sxs-lookup"><span data-stu-id="dbe74-107">The rest of the code is a short character string to describe the condition.</span></span> <span data-ttu-id="dbe74-108">Cada palavra na cadeia de caracteres é separada por um caractere de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="dbe74-108">Each word in the string is separated by an underscore.</span></span> <span data-ttu-id="dbe74-109">Por exemplo, o valor de erro MAPI_E_TOO_COMPLEX indica que a implementação não pôde tratar qualquer item estava sendo solicitado na chamada.</span><span class="sxs-lookup"><span data-stu-id="dbe74-109">For example, the error value MAPI_E_TOO_COMPLEX indicates that the implementation could not handle whatever was being requested in the call.</span></span> <span data-ttu-id="dbe74-110">O valor de aviso MAPI_W_PARTIAL_COMPLETION indica que a chamada foi bem-sucedida, mas houve problemas.</span><span class="sxs-lookup"><span data-stu-id="dbe74-110">The warning value MAPI_W_PARTIAL_COMPLETION indicates that the call succeeded, but that there were problems.</span></span> <span data-ttu-id="dbe74-111">Somente a parte da operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="dbe74-111">Only part of the operation was completed successfully.</span></span>
  

