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
  
> [in] Um ponteiro para uma matriz que contém os nomes das classes de mensagem a resolver. Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla como as classes de mensagem são resolvidas. O sinalizador a seguir pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Somente cadeias de caracteres de classe de mensagem que sejam uma combinação exata devem ser resolvidas.
    
 _ppfrminfoarray_
  
> [out] Um ponteiro para um ponteiro para uma matriz de objetos de informações de formulário. Se um aplicativo cliente passar NULL no parâmetro  _pMsgClassArray,_ o parâmetro  _ppfrminfoarray_ conterá objetos de informações de formulário para todos os formulários no contêiner. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam o método **IMAPIFormContainer::ResolveMultipleMessageClasses** para resolver um grupo de classes de mensagens para formulários dentro de um contêiner de formulário. A matriz de objetos de informações de formulário retornados no  _parâmetro ppfrminfoarray_ fornece mais acesso a cada uma das propriedades dos formulários. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver um grupo de classes de mensagens para formulários, passe uma matriz de nomes de classe de mensagem a serem resolvidos. Para forçar a resolução a ser exata (ou seja, para evitar a resolução para uma classe base da classe de mensagem), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no _parâmetro ulFlags._ 
  
Se uma classe de mensagem não puder ser resolvida para um formulário, NULL será retornado para essa classe de mensagem na matriz de informações do formulário. Portanto, mesmo que o método retorne S_OK, não suponha que todas as classes de mensagens foram resolvidas com êxito. Em vez disso, verifique os valores na matriz retornada.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI uses the **IMAPIFormContainer::ResolveMultipleMessageClasses** method to locate a form that is associated with a set of message classes.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

