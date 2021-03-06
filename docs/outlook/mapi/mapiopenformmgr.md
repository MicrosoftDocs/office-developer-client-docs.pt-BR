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
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418047"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma [interface IMAPIFormMgr](imapiformmgriunknown.md) em um objeto de provedor de biblioteca de formulário no contexto de uma sessão existente. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
   
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
  
> [out] Ponteiro para a interface **IMAPIFormMgr retornada.** 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Depois que um aplicativo cliente faz uma chamada para a função **MAPIOpenFormMgr,** a maioria das interações relacionadas a formulários subsequentes ocorre através do provedor da biblioteca de formulários ou de uma interface retornada pelo provedor da biblioteca de formulários. A interface **IMAPIFormMgr** permite que o cliente trabalhe com manipuladores de mensagens e execute resoluções entre classes de mensagens e bibliotecas de formulário. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg.cpp abre o gerenciador de formulário para que um formulário possa ser selecionado.  <br/> |CMainDlg::OnSelectForm  <br/> |MFCMAPI usa o **método MAPIOpenFormMgr** para abrir o gerenciador de formulário para que um formulário possa ser selecionado.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

