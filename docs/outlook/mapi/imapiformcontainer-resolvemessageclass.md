---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408548"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Resolve uma classe de mensagem para seu formulário em um contêiner de formulário e retorna um objeto de informações de formulário para esse formulário.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Parâmetros

 _szMessageClass_
  
> [in] Uma cadeia de caracteres que nomeia a classe de mensagem que está sendo resolvida. Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla como a classe de mensagem é resolvida. O sinalizador a seguir pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Somente cadeias de caracteres de classe de mensagem que sejam uma combinação exata devem ser resolvidas.
    
 _ppforminfo_
  
> [out] Um ponteiro para um ponteiro para o objeto de informações de formulário retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_NOT_FOUND 
  
> A classe de mensagem passada no  _parâmetro szMessageClass_ não combina com a classe de mensagem de nenhum formulário no contêiner de formulário. 
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam o método **IMAPIFormContainer::ResolveMessageClass** para resolver uma classe de mensagem para um formulário dentro de um contêiner de formulário. O objeto de informações de formulário retornado no  _parâmetro ppforminfo_ fornece mais acesso às propriedades do formulário com a classe de mensagem determinada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver uma classe de mensagem para um formulário, passe o nome da classe de mensagem a ser resolvida (por exemplo,  `IPM.HelpDesk.Software` ). Para forçar a resolução a ser exata (ou seja, para evitar a resolução para uma classe base da classe de mensagem), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no _parâmetro ulFlags._ 
  
O identificador de classe para a classe de mensagem resolvida é retornado como parte do objeto de informações do formulário. Não suponha que o identificador de classe exista na biblioteca OLE até depois de chamar o método [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) ou [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI usa o **método IMAPIFormContainer::ResolveMessageClass** para localizar um formulário associado a uma classe de mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

