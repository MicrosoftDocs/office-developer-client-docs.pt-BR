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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426391"
---
# <a name="imapiformmgrresolvemessageclass"></a>IMAPIFormMgr::ResolveMessageClass

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Resolve uma classe de mensagem para seu formulário dentro de um contêiner de formulário e retorna um objeto de informações de formulário para esse formulário.
  
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
  
> [in] Uma bitmask de sinalizadores que controla como a classe de mensagem é resolvida. O sinalizador a seguir pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Somente cadeias de caracteres de classe de mensagem que sejam uma combinação exata devem ser resolvidas.
    
 _pFolderFocus_
  
> [in] Um ponteiro para a pasta que contém a mensagem que está sendo resolvida. O  _parâmetro pFolderFocus_ pode ser NULL. 
    
 _ppResult_
  
> [out] Um ponteiro para um ponteiro para um objeto de informações de formulário retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_NOT_FOUND 
  
> A classe de mensagem passada no  _parâmetro szMsgClass_ não combina com a classe de mensagem de nenhum formulário na biblioteca de formulário. 
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam o método **IMAPIFormMgr::ResolveMessageClass** para resolver uma classe de mensagem para seu formulário dentro de um contêiner de formulário. O objeto de informações de formulário retornado no  _parâmetro ppResult_ fornece mais acesso às propriedades do formulário que tem a classe de mensagem determinada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver uma classe de mensagem para um formulário, um visualizador de formulário passa o nome da classe de mensagem a ser resolvida, como " `IPM.HelpDesk.Software` ". Para forçar a resolução a ser exata (ou seja, para evitar a resolução para uma classe base da classe de mensagem quando um servidor de formulário exatamente correspondente não estiver disponível), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _ulFlags._ Se o  _parâmetro pFolderFocus_ for NULL, o processo de resolução de classe de mensagem não pesquisa um contêiner de pasta. 
  
A ordem dos contêineres pesquisados depende da implementação do provedor de biblioteca de formulário. O provedor de biblioteca de formulário padrão pesquisa primeiro o contêiner local, depois o contêiner da pasta passada, o contêiner de formulário pessoal e, por fim, o contêiner da organização.
  
Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.
  
O identificador de classe para a classe de mensagem resolvida é retornado como parte do objeto de informações do formulário. Um visualizador de formulário não deve trabalhar na suposição de que o identificador de classe existe na biblioteca OLE até que o visualizador de formulário tenha chamado o método [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) ou o método [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md) 
  
## <a name="see-also"></a>Confira também



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

