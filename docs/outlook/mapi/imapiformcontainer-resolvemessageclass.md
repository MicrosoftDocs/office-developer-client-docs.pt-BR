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
ms.openlocfilehash: 713a177d5ceddf5fd4d97a0e35d87b2250748faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767021"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**Aplica-se a**: Outlook 
  
Resolve uma classe de mensagem para o seu formulário em um contêiner de formulário e retorna um objeto de informações de formulário para nesse formulário.
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>Parâmetros

 _szMessageClass_
  
> [in] Uma cadeia de caracteres que nomeia a classe de mensagem que está sendo resolvida. Nomes de classe de mensagem são sempre cadeias de caracteres ANSI, Unicode nunca.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a classe da mensagem for resolvida. O seguinte sinalizador pode ser definido:
    
MAPIFORM_EXACTMATCH 
  
> Apenas mensagem classe cadeias de caracteres que são uma correspondência exata devem ser resolvidas.
    
 _ppforminfo_
  
> [out] Um ponteiro para um ponteiro para o objeto de informações do formulário retornado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
E_NOT_FOUND 
  
> A classe de mensagem passada no parâmetro _szMessageClass_ não coincide com a classe de mensagem para qualquer formulário no contêiner do formulário. 
    
## <a name="remarks"></a>Comentários

Aplicativos cliente chamam o método de **IMAPIFormContainer::ResolveMessageClass** para resolver uma classe de mensagem para um formulário dentro de um contêiner de formulário. O objeto de informações do formulário retornado no parâmetro _ppforminfo_ fornece mais acesso às propriedades do formulário com a classe de mensagem determinado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para resolver uma classe de mensagem para um formulário, passar o nome de classe de mensagem a ser resolvido (por exemplo, `IPM.HelpDesk.Software`). Para forçar a resolução para ser exato (ou seja, para evitar a resolução para uma classe base da classe de mensagem), o sinalizador MAPIFORM_EXACTMATCH pode ser passado no parâmetro _ulFlags_ . 
  
O identificador de classe para a classe de mensagem resolvido é retornado como parte do objeto de informações de formulário. Não presuma que o identificador de classe existe na biblioteca do OLE até depois que você chama o método o [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) ou [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI usa o método **IMAPIFormContainer::ResolveMessageClass** para localizar um formulário que está associado uma classe de mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

