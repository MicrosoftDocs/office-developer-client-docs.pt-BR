---
title: Exemplos de código de restrição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b82097c-dbd6-4ba0-a6cb-292301f9402b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4f41abe2ee41946f68e1d79c75b36791364ea970
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770278"
---
# <a name="sample-restriction-code"></a><span data-ttu-id="62807-103">Exemplos de código de restrição</span><span class="sxs-lookup"><span data-stu-id="62807-103">Sample restriction code</span></span>

<span data-ttu-id="62807-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62807-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62807-105">O código de exemplo a seguir mostra como criar uma restrição que filtra todas as mensagens que não contêm a palavra "voleibol" na linha de assunto e não foram enviados a Suzana de Sam.</span><span class="sxs-lookup"><span data-stu-id="62807-105">The following sample code shows how to create a restriction that filters out all messages that do not contain the word "volleyball" in the subject line and were not sent to Sue from Sam.</span></span> <span data-ttu-id="62807-106">Uma árvore de estruturas [SRestriction](srestriction.md) será necessária, com o nó superior, sendo uma restrição **e** implementada com uma estrutura [SAndRestriction](sandrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="62807-106">A tree of [SRestriction](srestriction.md) structures is required, with the top node being an **AND** restriction implemented with an [SAndRestriction](sandrestriction.md) structure.</span></span> <span data-ttu-id="62807-107">As restrições de três que são reunidas pela operação de **AND** são uma restrição subobjeto que procura as mensagens enviadas para Sue, uma restrição de conteúdo que procura por mensagens de Sam e restrição **e** outra que procura por mensagens que possuírem um assunto contendo "voleibol."</span><span class="sxs-lookup"><span data-stu-id="62807-107">The three restrictions that are joined by the **AND** operation are a subobject restriction that searches for messages sent to Sue, a content restriction that searches for messages from Sam, and another **AND** restriction that searches for messages that have a subject containing "volleyball."</span></span> <span data-ttu-id="62807-108">Como **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) não é uma propriedade necessária, uma restrição **existem** deve ser incluída.</span><span class="sxs-lookup"><span data-stu-id="62807-108">Because **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) is not a required property, an **Exist** restriction must be included.</span></span> 
  
<span data-ttu-id="62807-109">Este código usa alocação dinâmica e inicialização; é possível alocar e inicializar estaticamente também.</span><span class="sxs-lookup"><span data-stu-id="62807-109">This code uses dynamic allocation and initialization; it is possible to allocate and initialize statically as well.</span></span> <span data-ttu-id="62807-110">Para fins de concisão, a verificação de erros ocorridos devem seguir as chamadas de alocação não está incluído na amostra.</span><span class="sxs-lookup"><span data-stu-id="62807-110">In the interest of brevity, the error checking that must occur following the allocation calls is not included in the sample.</span></span> 
  
```cpp
HRESULT BuildRestriction (LPSTR pszSent, LPSTR pszFrom,
                                LPSTR pszSubjectText);
{
    LPSRestriction pRest, pAndRes, pObjRes, pSubjAndRes;
    LPSPropValue pRecip, pSender, pSubject;
    HRESULT hResult;
    ULONG ulResCount = 3, ulSubjCount = 2
    // Allocate and build  restriction to join criteria
    hResult = MAPIAllocateMore (sizeof(SRestriction)*ulResCount, pRest,
            (LPVOID *)&pAndRes);
    pRest->rt = RES_AND;
    pRest->res.resAnd.cRes = ulResCount;
    pRest->res.resAnd.lpRes = pAndRes;
    // Allocate and build subobject restriction to search recipient list
    hResult = MAPIAllocateMore (sizeof(SRestriction), pRest,
            (LPVOID *)&pObjRes);
    pAndRes[0].rt = RES_SUBRESTRICTION;
    pAndRes[0].res.resSub.ulSubObject = PR_MESSAGE_RECIPIENTS;
    pAndRes[0].res.resSub.lpRes = pObjRes;
    // Allocate and build content restriction to look for recipient
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pRecip);
    pObjRes->rt = RES_CONTENT;
    pObjRes->res.resContent.ulFuzzyLevel =
            FL_FULLSTRING | FL_IGNORECASE;
    pObjRes->res.resContent.ulPropTag = pRecip->ulPropTag =
            PR_DISPLAY_NAME;
    pObjRes->res.resContent.lpProp = pRecip;
    pRecip->Value.LPSZ = pszSent;              // pszSent set to Sue
    // Allocate and build content restriction to look for sender
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSend);
    pAndRes[1].rt = RES_CONTENT;
    pAndRes[1].res.resContent.ulFuzzyLevel =
            FL_FULLSTRING | FL_IGNORECASE;
    pAndRes[1].res.resContent.ulPropTag = pSend->ulPropTag =
            PR_SENDER_NAME;
    pAndRes[1].res.resContent.lpProp = pSend;
    pSend->Value.LPSZ = pszName;                    // pszName set to Sam
    // Allocate and build  restriction to look for subject
    hResult = MAPIAllocateMore (sizeof(SRestriction)*ulSubjCount, pRest,
            (LPVOID *)&pSubjAndRes);
    pRest->rt = RES_AND;
    pRest->res.resAnd.cRes = ulResCount;
    pRest->res.resAnd.lpRes = pAndRes;
    // Create an  restriction to search for subject
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubjAndRes);
    pAndRes[2].rt = RES_AND;
    pAndRes[2].res.resAnd.cRes = ulSubjCount;
    pAndRes[2].res.resAnd.lpRes = pSubjAndRes;
    // Exist restriction to check that PR_SUBJECT exists
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubj);
    pSubjAndRes[0].rt = RES_EXIST;
    pSubjAndRes[0].res.resExist.ulReserved1 = 0;
    pSubjAndRes[0].res.resExist.ulReserved2 = 0;
    pSubjAndRes[0].res.resExist.ulPropTag = PR_SUBJECT;
    // Content restriction to check for "volleyball" in subject
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubj);
    pSubjAndRes[1].res.resContent.ulFuzzyLevel =
            FL_SUBSTRING | FL_IGNORECASE;
    pSubjAndRes[1].res.resContent.ulPropTag = pSubj->ulPropTag =
            PR_SUBJECT;
    pSubjAndRes[1].res.resContent.lpProp = pSubj;
    pSubj->Value.LPSZ = pszSubjectText;
    return hResult;
}
 
```

## <a name="see-also"></a><span data-ttu-id="62807-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="62807-111">See also</span></span>

- [<span data-ttu-id="62807-112">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="62807-112">MAPI Tables</span></span>](mapi-tables.md)

