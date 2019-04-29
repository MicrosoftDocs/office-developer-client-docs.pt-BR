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
  
> no Uma cadeia de caracteres que nomeia a classe da mensagem que está sendo resolvida. Os nomes de classe de mensagem são sempre cadeias de caracteres ANSI, nunca Unicode.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a classe da mensagem é resolvida. O seguinte sinalizador pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Somente as cadeias de caracteres de classe de mensagem que têm uma correspondência exata devem ser resolvidas.
    
 _ppforminfo_
  
> bota Um ponteiro para um ponteiro para o objeto de informações do formulário retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NOT_FOUND 
  
> A classe de mensagem passada no parâmetro _szMessageClass_ não corresponde à classe de mensagem de nenhum formulário no contêiner de formulários. 
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam o método **IMAPIFormContainer:: ResolveMessageClass** para resolver uma classe de mensagem para um formulário dentro de um contêiner de formulários. O objeto de informações de formulário retornado no parâmetro _ppforminfo_ fornece acesso adicional às propriedades do formulário com a classe de mensagem determinada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver uma classe de mensagem para um formulário, passe o nome da classe da mensagem a ser resolvida (por exemplo `IPM.HelpDesk.Software`,). Para forçar a resolução a ser exata (ou seja, para impedir a resolução de uma classe base da classe Message), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _parâmetroulflags_ . 
  
O identificador de classe da classe de mensagem resolvida é retornado como parte do objeto de informações do formulário. Não presuma que o identificador de classe existe na biblioteca OLE até que você chame o método [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) ou [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) . 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FormContainerDlg. cpp  <br/> |CFormContainerDlg:: OnResolveMessageClass  <br/> |MFCMAPI usa o método **IMAPIFormContainer:: ResolveMessageClass** para localizar um formulário que é associado a uma classe de mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

