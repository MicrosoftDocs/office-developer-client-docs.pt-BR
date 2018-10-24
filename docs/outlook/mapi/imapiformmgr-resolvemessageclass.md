---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3cd84e4ddb6d722d9f3de11d65b100d86e69ecae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571812"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Resolve uma classe de mensagem para o seu formulário dentro de um contêiner de formulário e retorna um objeto de informações de formulário para nesse formulário.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a>Parâmetros

 _szMsgClass_
  
> [in] Uma cadeia de caracteres que nomeia a classe de mensagem que está sendo resolvida.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a classe da mensagem for resolvida. O seguinte sinalizador pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Apenas mensagem classe cadeias de caracteres que são uma correspondência exata devem ser resolvidas.
    
 _pFolderFocus_
  
> [in] Um ponteiro para a pasta que contém a mensagem que está sendo resolvida. O parâmetro _pFolderFocus_ pode ser NULL. 
    
 _ppResult_
  
> [out] Um ponteiro para um ponteiro para um objeto de informações do formulário retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
E_NOT_FOUND 
  
> A classe de mensagem passada no parâmetro _szMsgClass_ não coincide com a classe de mensagem para qualquer formulário na biblioteca de formulários. 
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIFormMgr::ResolveMessageClass** para resolver uma classe de mensagem para o seu formulário dentro de um contêiner de formulário. O objeto de informações do formulário retornado no parâmetro _ppResult_ fornece mais acesso às propriedades do formulário que tem a classe de mensagem determinado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver uma classe de mensagem para um formulário, um visualizador de formulário passa no nome de classe de mensagem ser resolvidos, como " `IPM.HelpDesk.Software`". Para forçar a resolução para ser exato (ou seja, para evitar a resolução para uma classe base da classe de mensagem quando um formulário exatamente correspondente server não está disponível), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _ulFlags_ . Se o parâmetro _pFolderFocus_ for NULL, o processo de resolução de classe de mensagem não procura um contêiner de pasta. 
  
A ordem dos contêineres pesquisadas depende a implementação do provedor de biblioteca de formulário. O provedor de biblioteca de formulário padrão pesquisa primeiro o contêiner de local, em seguida, o contêiner de pasta para a pasta de no passado, o contêiner de formulários particular e, por fim, o contêiner da organização.
  
Nomes de classe de mensagem são sempre cadeias de caracteres ANSI, Unicode nunca.
  
O identificador de classe para a classe de mensagem resolvido é retornado como parte do objeto de informações de formulário. Um visualizador de formulário não deve funcionar no pressuposto de que o identificador de classe existe na biblioteca do OLE até depois que a tela de formulário tiver chamado o método [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) ou o método [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

