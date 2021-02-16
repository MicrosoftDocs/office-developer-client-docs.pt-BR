---
title: Remover a definição de formulário personalizada salva com uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: ac162cb73cfdee83bf034de32064c5ed9df3bc02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408464"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a><span data-ttu-id="66ff3-103">Remover a definição de formulário personalizada salva com uma mensagem</span><span class="sxs-lookup"><span data-stu-id="66ff3-103">Remove custom form definition saved with a message</span></span>
  
<span data-ttu-id="66ff3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66ff3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66ff3-105">Este tópico mostra um exemplo de código em C++ que converte uma mensagem que foi salva com uma definição de formulário personalizada em uma mensagem regular sem a definição do formulário.</span><span class="sxs-lookup"><span data-stu-id="66ff3-105">This topic shows a code sample in C++ that converts a message that has been saved with a custom form definition to a regular message without the form definition.</span></span>
  
<span data-ttu-id="66ff3-106">No Microsoft Outlook 2010 ou no Microsoft Outlook 2013, você pode compartilhar formulários contendo páginas de formulário personalizadas publicando-as em uma biblioteca de formulários ou salvando a definição de formulário correspondente com uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="66ff3-106">In Microsoft Outlook 2010 or Microsoft Outlook 2013, you can share forms containing custom form pages by either publishing them to a forms library or saving the corresponding form definition with a message.</span></span> <span data-ttu-id="66ff3-107">Um formulário personalizado salvo com uma mensagem normalmente é chamado de "formulário único", já que o formulário é compartilhado apenas para exibir essa mensagem específica como uma instância única.</span><span class="sxs-lookup"><span data-stu-id="66ff3-107">A custom form saved with a message is commonly referred as a "one-off form", since the form is shared only for viewing that specific message as a one-off instance.</span></span> <span data-ttu-id="66ff3-108">Você normalmente faz isso quando o formulário não é publicado em uma biblioteca de formulários, mas deseja que o destinatário use o formulário personalizado ao abrir o item.</span><span class="sxs-lookup"><span data-stu-id="66ff3-108">You typically do this when the form is not published in a forms library but you want the recipient to use the custom form when opening the item.</span></span> <span data-ttu-id="66ff3-109">You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form.</span><span class="sxs-lookup"><span data-stu-id="66ff3-109">You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form.</span></span> 
  
<span data-ttu-id="66ff3-110">Formulários que contêm páginas de formulário podem ser personalizados com código no Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="66ff3-110">Forms containing form pages can be customized with code in Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="66ff3-111">As mensagens salvas com definições de formulário geralmente têm um tamanho maior.</span><span class="sxs-lookup"><span data-stu-id="66ff3-111">Messages that are saved with form definitions are generally bigger in size.</span></span> <span data-ttu-id="66ff3-112">Por motivos de segurança e armazenamento, o Outlook 2010 e o Outlook 2013 ignoram definições de formulário salvas com qualquer item.</span><span class="sxs-lookup"><span data-stu-id="66ff3-112">For security and storage reasons, Outlook 2010 and Outlook 2013 ignore form definitions saved with any item.</span></span>
  
<span data-ttu-id="66ff3-113">Para converter uma mensagem salva com uma definição de formulário personalizada em uma sem, você deve remover quatro propriedades nomeadas:</span><span class="sxs-lookup"><span data-stu-id="66ff3-113">To convert a message that is saved with a custom form definition to one without, you must remove four named properties:</span></span>
  
- [<span data-ttu-id="66ff3-114">Propriedade can�nico de PidLidFormStorage</span><span class="sxs-lookup"><span data-stu-id="66ff3-114">PidLidFormStorage Canonical Property</span></span>](pidlidformstorage-canonical-property.md)
    
- [<span data-ttu-id="66ff3-115">Propriedade can�nico de PidLidPageDirStream</span><span class="sxs-lookup"><span data-stu-id="66ff3-115">PidLidPageDirStream Canonical Property</span></span>](pidlidpagedirstream-canonical-property.md)
    
- [<span data-ttu-id="66ff3-116">Propriedade can�nico de PidLidFormPropStream</span><span class="sxs-lookup"><span data-stu-id="66ff3-116">PidLidFormPropStream Canonical Property</span></span>](pidlidformpropstream-canonical-property.md)
    
- [<span data-ttu-id="66ff3-117">Propriedade can�nico de PidLidScriptStream</span><span class="sxs-lookup"><span data-stu-id="66ff3-117">PidLidScriptStream Canonical Property</span></span>](pidlidscriptstream-canonical-property.md)
    
<span data-ttu-id="66ff3-118">Além disso, você também deve remover a propriedade canônica [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) que contém as definições de propriedades personalizadas salvas com essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="66ff3-118">In addition, you should also remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) that contains the definitions of custom properties saved with that message.</span></span> <span data-ttu-id="66ff3-119">Um efeito colateral da remoção dessa propriedade é que os modelos de objeto do Outlook 2010 ou do Outlook 2013 e a interface do usuário do Outlook 2010 ou do Outlook 2013 não poderão mais acessar as propriedades do usuário que foram definidas na mensagem.</span><span class="sxs-lookup"><span data-stu-id="66ff3-119">A side effect of removing this property is that the Outlook 2010 or Outlook 2013 object models and the Outlook 2010 or Outlook 2013 user interface will no longer be able to access user properties that have been set on the message.</span></span> <span data-ttu-id="66ff3-120">Você ainda pode acessar essas propriedades e seus valores por meio de MAPI.</span><span class="sxs-lookup"><span data-stu-id="66ff3-120">You are still able to access these properties and their values through MAPI.</span></span> <span data-ttu-id="66ff3-121">Observe que, se você não remover essa propriedade e a mensagem for salva com outra definição de formulário, a propriedade canônica [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) será parcialmente substituída por novos dados e a integridade dos dados não será garantida.</span><span class="sxs-lookup"><span data-stu-id="66ff3-121">Note that if you do not remove this property and the message is saved with another form definition, the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md) is partially overwritten with new data and data integrity is not guaranteed.</span></span> 
  
<span data-ttu-id="66ff3-122">Se você remover a propriedade canônica [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md), você também deve remover o sinalizador **INSP_PROPDEFINITION** da propriedade canônica [PidLidCustomFlag](pidlidcustomflag-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="66ff3-122">If you remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md), then you should also remove the **INSP_PROPDEFINITION** flag from the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md).</span></span>
  
<span data-ttu-id="66ff3-123">A função a seguir, aceita como parâmetros de entrada um ponteiro para uma mensagem e um indicador se a propriedade canônica  `RemoveOneOff` [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="66ff3-123">The following function,  `RemoveOneOff`, accepts as input parameters a pointer to a message and an indicator whether to remove the [PidLidPropertyDefinitionStream Canonical Property](pidlidpropertydefinitionstream-canonical-property.md).</span></span> <span data-ttu-id="66ff3-124">Usando o ponteiro da mensagem, ele chama [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter os identificadores de propriedade apropriados e chama [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) para remover as propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="66ff3-124">Using the message pointer, it calls [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the appropriate property identifiers, and then calls [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) to remove the named properties.</span></span> <span data-ttu-id="66ff3-125">Ele também chama [IMAPIProp::GetProps](imapiprop-getprops.md) para obter a propriedade canônica [PidLidCustomFlag](pidlidcustomflag-canonical-property.md) e limpa o sinalizador **\_ ONEOFFFLAGS do INSP** e o sinalizador **INSP_PROPDEFINITION** conforme apropriado dessa propriedade, para que o Outlook 2010 e o Outlook 2013 não procure as propriedades nomeadas que foram removidas.</span><span class="sxs-lookup"><span data-stu-id="66ff3-125">It also calls [IMAPIProp::GetProps](imapiprop-getprops.md) to get the [PidLidCustomFlag Canonical Property](pidlidcustomflag-canonical-property.md) and clears the **INSP\_ONEOFFFLAGS** flag and **INSP_PROPDEFINITION** flag as appropriate from that property, so that Outlook 2010 and Outlook 2013 will not look for those named properties that have been removed.</span></span> 
  
```cpp
ULONG aulOneOffIDs[] = {dispidFormStorage,  
    dispidPageDirStream, 
    dispidFormPropStream, 
    dispidScriptStream, 
    dispidPropDefStream, // dispidPropDefStream must remain next to last in list 
    dispidCustomFlag};   // dispidCustomFlag must remain last in list 
 
#define ulNumOneOffIDs (sizeof(aulOneOffIDs)/sizeof(aulOneOffIDs[0])) 
 
HRESULT RemoveOneOff(LPMESSAGE lpMessage, BOOL bRemovePropDef) 
{ 
    if (!lpMessage) return MAPI_E_INVALID_PARAMETER; 
     
    HRESULT hRes = S_OK; 
    MAPINAMEID  rgnmid[ulNumOneOffIDs]; 
    LPMAPINAMEID rgpnmid[ulNumOneOffIDs]; 
    LPSPropTagArray lpTags = NULL; 
 
    ULONG i = 0; 
    for (i = 0 ; i < ulNumOneOffIDs ; i++) 
    { 
        rgnmid[i].lpguid = (LPGUID)&PSETID_Common; 
        rgnmid[i].ulKind = MNID_ID; 
        rgnmid[i].Kind.lID = aulOneOffIDs[i]; 
        rgpnmid[i] = &rgnmid[i]; 
    } 
   
    hRes = lpMessage->GetIDsFromNames( 
        ulNumOneOffIDs, 
        rgpnmid, 
        0, 
        &lpTags); 
    if (lpTags) 
    { 
        // The last prop is the flag value  
        // to be updated, don't count it 
        lpTags->cValues = ulNumOneOffIDs-1; 
 
        // If the prop def stream is not to be removed, don't count it 
        if (!bRemovePropDef) 
        { 
          lpTags->cValues = lpTags->cValues-1; 
        } 
 
        hRes = lpMessage->DeleteProps( 
            lpTags, 
            0); 
        if (SUCCEEDED(hRes)) 
        { 
            SPropTagArray pTag = {0}; 
            ULONG cProp = 0; 
            LPSPropValue lpCustomFlag = NULL; 
 
            // Grab dispidCustomFlag, the last tag in the array 
            pTag.cValues = 1; 
            pTag.aulPropTag[0] = CHANGE_PROP_TYPE( 
                lpTags->aulPropTag[ulNumOneOffIDs-1], 
                PT_LONG); 
 
            hRes = lpMessage->GetProps( 
                &pTag, 
                fMapiUnicode, 
                &cProp, 
                &lpCustomFlag); 
            if (SUCCEEDED(hRes) &&  
                1 == cProp && lpCustomFlag &&  
                PT_LONG == PROP_TYPE(lpCustomFlag->ulPropTag)) 
            { 
                // Clear the INSP_ONEOFFFLAGS bits so Outlook  
                // doesn't look for the props that have been deleted 
                lpCustomFlag->Value.l =  
                    lpCustomFlag->Value.l & ~(INSP_ONEOFFFLAGS); 
                if (bRemovePropDef) 
                { 
                    lpCustomFlag->Value.l =  
                        lpCustomFlag->Value.l & ~(INSP_PROPDEFINITION); 
                } 
                hRes = lpMessage->SetProps( 
                    1, 
                    lpCustomFlag, 
                    NULL); 
             } 
 
             hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE); 
         } 
    } 
    MAPIFreeBuffer(lpTags); 
 
    return hRes; 
}
```

## <a name="see-also"></a><span data-ttu-id="66ff3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="66ff3-126">See also</span></span>

- [<span data-ttu-id="66ff3-127">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="66ff3-127">MAPI Constants</span></span>](mapi-constants.md)

