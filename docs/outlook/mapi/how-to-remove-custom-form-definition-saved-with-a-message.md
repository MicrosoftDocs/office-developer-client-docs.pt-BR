---
title: Remova a definição de formulário personalizado salva com uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6a270f0c-104a-84a1-9adf-aea166f89071
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 4b12824542a1408a364452eb6587122ec66412d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594450"
---
# <a name="remove-custom-form-definition-saved-with-a-message"></a>Remova a definição de formulário personalizado salva com uma mensagem
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico mostra um exemplo de código em C++ que converte uma mensagem que tenha sido salva com uma definição de formulário personalizado para uma mensagem regular sem a definição do formulário.
  
No Microsoft Outlook 2010 ou o Microsoft Outlook 2013, você pode compartilhar formulários que contém as páginas de formulário personalizado por publicá-los em uma biblioteca de formulários ou salvar a definição de formulário correspondente com uma mensagem. Um formulário personalizado salvo com uma mensagem é normalmente conhecido como "formulário one-off", desde que o formulário é compartilhado apenas para exibição essa mensagem específica como uma instância único. Você normalmente faz isso quando o formulário não é publicado em uma biblioteca de formulários, mas quer que o destinatário use o formulário personalizado ao abrir o item. Você pode especificar que um formulário é um one-off no Designer de formulários, marcando a caixa de seleção **Enviar definição do formulário com item** na página **Propriedades** do formulário. 
  
Formulários que contém as páginas de formulário podem ser personalizados com código no Visual Basic Scripting Edition (VBScript). Mensagens que são salvas com as definições de formulário são geralmente maiores em tamanho. Por razões de armazenamento e de segurança, o Outlook 2010 e o Outlook 2013 ignoram definições do formulário salvas com qualquer item.
  
Para converter uma mensagem que é salvo com uma definição de formulário personalizado para aquele sem, você deve remover quatro propriedades nomeadas:
  
- [Propriedade can�nico de PidLidFormStorage](pidlidformstorage-canonical-property.md)
    
- [Propriedade can�nico de PidLidPageDirStream](pidlidpagedirstream-canonical-property.md)
    
- [Propriedade can�nico de PidLidFormPropStream](pidlidformpropstream-canonical-property.md)
    
- [Propriedade can�nico de PidLidScriptStream](pidlidscriptstream-canonical-property.md)
    
Além disso, você também deve remover a [Propriedade canônico de PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) que contém as definições das propriedades personalizadas salvas com a mensagem. Um efeito de remover essa propriedade é que os modelos de objeto do Outlook 2010 ou Outlook 2013 e a interface de usuário do Outlook 2010 ou Outlook 2013 não será possível acessar propriedades de usuário que foram definidas na mensagem. Você está ainda poderão acessar essas propriedades e seus valores por meio de MAPI. Observe que, se você não remover essa propriedade e a mensagem será salva com outra definição de formulário, a [Propriedade canônico de PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) parcialmente será substituído com novos dados e não há garantia de integridade dos dados. 
  
Se você remover a [Propriedade canônico de PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md), também devem remover o sinalizador **INSP_PROPDEFINITION** da [Propriedade canônico de PidLidCustomFlag](pidlidcustomflag-canonical-property.md).
  
A função a seguir, `RemoveOneOff`, aceita como parâmetros de entrada um ponteiro para uma mensagem e um indicador se deseja remover a [Propriedade canônico de PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md). Usando o ponteiro de mensagem, ela chama [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter os identificadores de propriedade apropriada e então chama [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) para remover as propriedades nomeadas. Ele também chama [IMAPIProp::GetProps](imapiprop-getprops.md) para obter a [Propriedade canônico de PidLidCustomFlag](pidlidcustomflag-canonical-property.md) e limpa o **INSP\_ONEOFFFLAGS** sinalizador e **INSP_PROPDEFINITION** sinalizar conforme apropriado nessa propriedade, assim que o Outlook 2010 e Outlook 2013 não procurará essas propriedades nomeadas que foram removidas. 
  
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

- [Constantes MAPI](mapi-constants.md)

