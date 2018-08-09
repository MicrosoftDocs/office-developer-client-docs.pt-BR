---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 592bd2c88c8eea17d80fe7cb725b075235c51763
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767997"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**Aplica-se a**: Outlook 
  
Abre uma interface de [IMAPIFormMgr](imapiformmgriunknown.md) em um objeto de provedor de biblioteca de formulário no contexto de uma sessão existente. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a>Parâmetros

 _pSession_
  
> [in] Ponteiro para a sessão em uso pelo aplicativo cliente.
    
 _ppmgr_
  
> [out] Ponteiro para a interface de **IMAPIFormMgr** retornado. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Depois que um aplicativo cliente faz uma chamada para a função **MAPIOpenFormMgr** , a maioria das interações subsequentes relacionados a formulários ocorrem por meio do provedor de biblioteca de formulário ou uma interface retornados pelo provedor de biblioteca de formulário. A interface de **IMAPIFormMgr** permite que o cliente trabalhar com manipuladores de mensagens e executar resoluções entre as classes de mensagem e bibliotecas de formulários. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp abre o Gerenciador de formulário para que um formulário pode ser selecionado.  <br/> |CMainDlg::OnSelectForm  <br/> |MFCMAPI usa o método **MAPIOpenFormMgr** para abrir o Gerenciador de formulário para que um formulário pode ser selecionado.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

