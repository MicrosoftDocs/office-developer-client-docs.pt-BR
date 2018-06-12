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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ad2014d1d003a4d80646ed1b679f0d3827341c1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767050"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**Aplica-se a**: Outlook 
  
Resolve um grupo de classes de mensagens para seus formulários dentro de um contêiner de formulário e retorna uma matriz de formulário objetos de informações para esses formulários.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Par�metros

 _pMsgClasses_
  
> [in] Um ponteiro para uma matriz que contém os nomes das classes de mensagem para resolver.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como as classes de mensagens forem resolvidas. O seguinte sinalizador pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Apenas mensagem classe cadeias de caracteres que são uma correspondência exata devem ser resolvidas.
    
MAPIFORM_LOCALONLY
  
> Não inclua formulários armazenados em cache.
    
 _pFolderFocus_
  
> [in] Um ponteiro para a pasta que contém o formulário cujo classe de mensagem está sendo resolvido. O parâmetro _pFolderFocus_ pode ser NULL. 
    
 _ppfrminfoarray_
  
> [out] Um ponteiro para um ponteiro para uma matriz de objetos de informações do formulário. Se um visualizador de formulário transmite NULL no parâmetro _pMsgClasses_ , o parâmetro _ppfrminfoarray_ contém objetos de informações de formulário para todos os formulários no contêiner. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Coment�rios

Visualizadores de formulário chame o método de **IMAPIFormMgr::ResolveMultipleMessageClasses** para resolver um grupo de classes de mensagens para formulários dentro de um contêiner de formulário. A matriz de objetos do formulário informações retornadas nos _ppfrminfoarray_ fornece mais acesso a cada uma das propriedades formas a. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver um grupo de classes de mensagens para formulários, um visualizador de formulário passa em uma matriz de nomes de classe de mensagem a ser resolvido. Para forçar a resolução para ser exato (ou seja, para evitar a resolução para uma classe base da classe de mensagem quando um formulário exatamente correspondente servidor não está disponível) o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _ulFlags_ . 
  
Nomes de classe de mensagem são sempre cadeias de caracteres ANSI, Unicode nunca.
  
Se uma classe de mensagem não pode ser resolvida para um formulário, NULL é retornada para essa classe de mensagem da matriz de informações do formulário. Portanto, mesmo se o método retorna S_OK, visualizadores do formulário não devem funcionar no pressuposto de que todas as classes de mensagem foram resolvidas com êxito. Em vez disso, os visualizadores de formulário devem verificar os valores na matriz retornada.
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)

