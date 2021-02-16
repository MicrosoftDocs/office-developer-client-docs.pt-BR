---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428015"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Resolve um grupo de classes de mensagem para seus formulários dentro de um contêiner de formulário e retorna uma matriz de objetos de informações de formulário para esses formulários.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parâmetros

 _pMsgClasses_
  
> [in] Um ponteiro para uma matriz que contém os nomes das classes de mensagem a resolver.
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla como as classes de mensagem são resolvidas. O sinalizador a seguir pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Somente cadeias de caracteres de classe de mensagem que sejam uma combinação exata devem ser resolvidas.
    
MAPIFORM_LOCALONLY
  
> Não inclua formulários armazenados em cache.
    
 _pFolderFocus_
  
> [in] Um ponteiro para a pasta que contém o formulário cuja classe de mensagem está sendo resolvida. O  _parâmetro pFolderFocus_ pode ser NULL. 
    
 _ppfrminfoarray_
  
> [out] Um ponteiro para um ponteiro para uma matriz de objetos de informações de formulário. Se um visualizador de formulários passar NULL no parâmetro  _pMsgClasses,_ o parâmetro  _ppfrminfoarray_ conterá objetos de informações de formulário para todos os formulários no contêiner. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam o método **IMAPIFormMgr::ResolveMultipleMessageClasses** para resolver um grupo de classes de mensagens para formulários dentro de um contêiner de formulário. A matriz de objetos de informações de formulário  _retornados em ppfrminfoarray_ fornece mais acesso a cada uma das propriedades dos formulários. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver um grupo de classes de mensagens para formulários, um visualizador de formulários passa uma matriz de nomes de classe de mensagem a serem resolvidos. Para forçar a resolução a ser exata (ou seja, para evitar a resolução para uma classe base da classe de mensagem quando um servidor de formulário exatamente correspondente não estiver disponível), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _ulFlags._ 
  
Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.
  
Se uma classe de mensagem não puder ser resolvida para um formulário, NULL será retornado para essa classe de mensagem na matriz de informações do formulário. Portanto, mesmo que o método retorne S_OK, os visualizadores de formulário não devem trabalhar com a suposição de que todas as classes de mensagens foram resolvidas com êxito. Em vez disso, os visualizadores de formulário devem verificar os valores na matriz retornada.
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

