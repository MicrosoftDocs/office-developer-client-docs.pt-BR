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
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321606"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Resolve uma classe de mensagem para seu formulário dentro de um contêiner de formulários e retorna um objeto de informações de formulário para esse formulário.
  
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
  
> no Uma cadeia de caracteres que nomeia a classe da mensagem que está sendo resolvida.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a classe da mensagem é resolvida. O seguinte sinalizador pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Somente as cadeias de caracteres de classe de mensagem que têm uma correspondência exata devem ser resolvidas.
    
 _pFolderFocus_
  
> no Um ponteiro para a pasta que contém a mensagem que está sendo resolvida. O parâmetro _pFolderFocus_ pode ser NULL. 
    
 _ppResult_
  
> bota Um ponteiro para um ponteiro para um objeto de informações do formulário retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NOT_FOUND 
  
> A classe de mensagem passada no parâmetro _szMsgClass_ não corresponde à classe de mensagem de nenhum formulário na biblioteca de formulários. 
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormMgr:: ResolveMessageClass** para resolver uma classe de mensagem para seu formulário dentro de um contêiner de formulários. O objeto de informações de formulário retornado no parâmetro _ppResult_ fornece acesso adicional às propriedades do formulário que tem a classe de mensagem determinada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver uma classe de mensagem para um formulário, um visualizador de formulários passa o nome da classe de mensagem a ser resolvida, como `IPM.HelpDesk.Software`"". Para forçar a resolução a ser exata (ou seja, para impedir a resolução de uma classe base da classe de mensagem quando um servidor de formulário com correspondência exata não estiver disponível), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _parâmetroulflags_ . Se o parâmetro _pFolderFocus_ for NULL, o processo de resolução da classe de mensagem não pesquisará um contêiner de pasta. 
  
A ordem dos contêineres pesquisada depende da implementação do provedor de biblioteca de formulários. O provedor de biblioteca de formulários padrão pesquisa primeiro o contêiner local e, em seguida, o contêiner de pasta para a pasta passada, o contêiner de formulário pessoal e, por fim, o contêiner da organização.
  
Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.
  
O identificador de classe da classe de mensagem resolvida é retornado como parte do objeto de informações do formulário. Um visualizador de formulários não deve funcionar na pressuposição de que o identificador de classe existe na biblioteca OLE até que o Visualizador de formulários tenha chamado o método [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) ou o método [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

