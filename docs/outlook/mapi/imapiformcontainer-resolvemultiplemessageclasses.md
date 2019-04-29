---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412538"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Resolve um grupo de classes de mensagem para seus formulários em um contêiner de formulário e retorna uma matriz de objetos de informações de formulário para esses formulários.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parâmetros

 _pMsgClassArray_
  
> no Um ponteiro para uma matriz que contém os nomes das classes de mensagens a serem resolvidas. Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como as classes de mensagem são resolvidas. O seguinte sinalizador pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Somente as cadeias de caracteres de classe de mensagem que têm uma correspondência exata devem ser resolvidas.
    
 _ppfrminfoarray_
  
> bota Um ponteiro para um ponteiro para uma matriz de objetos de informação do formulário. Se um aplicativo cliente passar nulo no parâmetro _pMsgClassArray_ , o parâmetro _ppfrminfoarray_ conterá objetos de informações de formulário para todos os formulários no contêiner. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam o método **IMAPIFormContainer:: ResolveMultipleMessageClasses** para resolver um grupo de classes de mensagem para formulários dentro de um contêiner de formulários. A matriz de objetos de informações de formulário retornada no parâmetro _ppfrminfoarray_ fornece acesso adicional a cada uma das propriedades de formulários. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver um grupo de classes de mensagem para formulários, passe uma matriz de nomes de classe de mensagem a ser resolvida. Para forçar a resolução a ser exata (ou seja, para impedir a resolução de uma classe base da classe Message), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _parâmetroulflags_ . 
  
Se uma classe de mensagem não puder ser resolvida para um formulário, NULL será retornado para essa classe de mensagem na matriz de informações do formulário. Portanto, mesmo que o método retorne S_OK, não presuma que todas as classes de mensagem tenham sido resolvidas com êxito. Em vez disso, verifique os valores na matriz retornada.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnResolveMultipleMessageClasses  <br/> |MFCMAPI usa o método **IMAPIFormContainer:: ResolveMultipleMessageClasses** para localizar um formulário que é associado a um conjunto de classes de mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

