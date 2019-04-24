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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321865"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Resolve um grupo de classes de mensagem para seus formulários dentro de um contêiner de formulários e retorna uma matriz de objetos de informações de formulário para esses formulários.
  
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
  
> no Um ponteiro para uma matriz que contém os nomes das classes de mensagens a serem resolvidas.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como as classes de mensagem são resolvidas. O seguinte sinalizador pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Somente as cadeias de caracteres de classe de mensagem que têm uma correspondência exata devem ser resolvidas.
    
MAPIFORM_LOCALONLY
  
> Não inclua formulários armazenados em cache.
    
 _pFolderFocus_
  
> no Um ponteiro para a pasta que contém o formulário cuja classe de mensagem está sendo resolvida. O parâmetro _pFolderFocus_ pode ser NULL. 
    
 _ppfrminfoarray_
  
> bota Um ponteiro para um ponteiro para uma matriz de objetos de informação do formulário. Se um visualizador de formulários passar nulo no parâmetro _pMsgClasses_ , o parâmetro _ppfrminfoarray_ contém objetos de informações de formulário para todos os formulários no contêiner. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormMgr:: ResolveMultipleMessageClasses** para resolver um grupo de classes de mensagem para formulários dentro de um contêiner de formulários. A matriz de objetos de informações de formulário retornada no _ppfrminfoarray_ fornece acesso adicional a cada uma das propriedades de formulários. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver um grupo de classes de mensagem para formulários, um visualizador de formulários passa em uma matriz de nomes de classe de mensagem a ser resolvida. Para forçar a resolução a ser exata (ou seja, para impedir a resolução de uma classe base da classe de mensagem quando um servidor de formulário com correspondência exata não estiver disponível), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _parâmetroulflags_ . 
  
Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.
  
Se uma classe de mensagem não puder ser resolvida para um formulário, NULL será retornado para essa classe de mensagem na matriz de informações do formulário. Portanto, mesmo que o método retorne S_OK, os visualizadores de formulário não devem funcionar na pressuposição de que todas as classes de mensagens tenham sido resolvidas com êxito. Em vez disso, os visualizadores de formulário devem verificar os valores na matriz retornada.
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

