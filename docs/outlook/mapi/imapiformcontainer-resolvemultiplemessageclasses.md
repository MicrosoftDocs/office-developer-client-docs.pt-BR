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
ms.openlocfilehash: c1da292943d6e4d9625c6ce37019c630471e200b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767026"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**Aplica-se a**: Outlook 
  
Resolve um grupo de classes de mensagens para seus formulários em um contêiner de formulário e retorna uma matriz de formulário objetos de informações para esses formulários.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parâmetros

 _pMsgClassArray_
  
> [in] Um ponteiro para uma matriz que contém os nomes das classes de mensagem para resolver. Nomes de classe de mensagem são sempre cadeias de caracteres ANSI, Unicode nunca.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como as classes de mensagens forem resolvidas. O seguinte sinalizador pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Apenas mensagem classe cadeias de caracteres que são uma correspondência exata devem ser resolvidas.
    
 _ppfrminfoarray_
  
> [out] Um ponteiro para um ponteiro para uma matriz de objetos de informações do formulário. Se um aplicativo cliente transmite NULL no parâmetro _pMsgClassArray_ , o parâmetro _ppfrminfoarray_ contém objetos de informações de formulário para todos os formulários no contêiner. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Aplicativos cliente chamam o método de **IMAPIFormContainer::ResolveMultipleMessageClasses** para resolver um grupo de classes de mensagens para formulários dentro de um contêiner de formulário. A matriz de objetos de informações de formulário retornado no parâmetro _ppfrminfoarray_ fornece mais acesso a cada uma das propriedades formas a. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver um grupo de classes de mensagens para formulários, passe uma matriz de nomes de classe de mensagem a ser resolvido. Para forçar a resolução para ser exato (ou seja, para evitar a resolução para uma classe base da classe de mensagem), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _ulFlags_ . 
  
Se uma classe de mensagem não pode ser resolvida para um formulário, NULL é retornada para essa classe de mensagem da matriz de informações do formulário. Portanto, mesmo se o método retorna S_OK, não presuma que todas as classes de mensagem foram resolvidas com êxito. Em vez disso, verifique os valores na matriz retornada.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI usa o método **IMAPIFormContainer::ResolveMultipleMessageClasses** para localizar um formulário que está associado um conjunto de classes de mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

