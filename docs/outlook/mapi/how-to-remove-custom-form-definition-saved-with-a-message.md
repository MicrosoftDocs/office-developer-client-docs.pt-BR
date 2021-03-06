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
# <a name="remove-custom-form-definition-saved-with-a-message"></a>Remover a definição de formulário personalizada salva com uma mensagem
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico mostra um exemplo de código em C++ que converte uma mensagem que foi salva com uma definição de formulário personalizada em uma mensagem regular sem a definição do formulário.
  
No Microsoft Outlook 2010 ou no Microsoft Outlook 2013, você pode compartilhar formulários contendo páginas de formulário personalizadas publicando-as em uma biblioteca de formulários ou salvando a definição de formulário correspondente com uma mensagem. Um formulário personalizado salvo com uma mensagem normalmente é chamado de "formulário único", já que o formulário é compartilhado apenas para exibir essa mensagem específica como uma instância única. Você normalmente faz isso quando o formulário não é publicado em uma biblioteca de formulários, mas deseja que o destinatário use o formulário personalizado ao abrir o item. You can specify a form is a one-off in the Forms Designer, by selecting the **Send form definition with item** check box on the **Properties** page of the form. 
  
Formulários que contêm páginas de formulário podem ser personalizados com código no Visual Basic Scripting Edition (VBScript). As mensagens salvas com definições de formulário geralmente têm um tamanho maior. Por motivos de segurança e armazenamento, o Outlook 2010 e o Outlook 2013 ignoram definições de formulário salvas com qualquer item.
  
Para converter uma mensagem salva com uma definição de formulário personalizada em uma sem, você deve remover quatro propriedades nomeadas:
  
- [Propriedade can�nico de PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Propriedade can�nico de PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Propriedade can�nico de PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Propriedade can�nico de PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
Além disso, você também deve remover a propriedade canônica [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) que contém as definições de propriedades personalizadas salvas com essa mensagem. Um efeito colateral da remoção dessa propriedade é que os modelos de objeto do Outlook 2010 ou do Outlook 2013 e a interface do usuário do Outlook 2010 ou do Outlook 2013 não poderão mais acessar as propriedades do usuário que foram definidas na mensagem. Você ainda pode acessar essas propriedades e seus valores por meio de MAPI. Observe que, se você não remover essa propriedade e a mensagem for salva com outra definição de formulário, a propriedade canônica [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) será parcialmente substituída por novos dados e a integridade dos dados não será garantida. 
  
Se você remover a propriedade canônica [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md), você também deve remover o sinalizador **INSP_PROPDEFINITION** da propriedade canônica [PidLidCustomFlag](pidlidcustomflag-canonical-property.md).
  
A função a seguir, aceita como parâmetros de entrada um ponteiro para uma mensagem e um indicador se a propriedade canônica  `RemoveOneOff` [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)deve ser removido. Usando o ponteiro da mensagem, ele chama [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter os identificadores de propriedade apropriados e chama [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) para remover as propriedades nomeadas. Ele também chama [IMAPIProp::GetProps](imapiprop-getprops.md) para obter a propriedade canônica [PidLidCustomFlag](pidlidcustomflag-canonical-property.md) e limpa o sinalizador **\_ ONEOFFFLAGS do INSP** e o sinalizador **INSP_PROPDEFINITION** conforme apropriado dessa propriedade, para que o Outlook 2010 e o Outlook 2013 não procure as propriedades nomeadas que foram removidas. 
  
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

## <a name="see-also"></a>Confira também

- [Constantes de MAPI](mapi-constants.md)

