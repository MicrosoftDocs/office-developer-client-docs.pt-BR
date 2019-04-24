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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270095"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma interface [IMAPIFormMgr](imapiformmgriunknown.md) em um objeto de provedor de biblioteca de formulários no contexto de uma sessão existente. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a>Parâmetros

 _pSession_
  
> no Ponteiro para a sessão em uso pelo aplicativo cliente.
    
 _ppmgr_
  
> bota Ponteiro para a interface **IMAPIFormMgr** retornada. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Depois que um aplicativo cliente faz uma chamada para a função **MAPIOpenFormMgr** , a maioria das interações relacionadas a formulários subsequentes acontece através do provedor de biblioteca de formulários ou de uma interface retornada pelo provedor de biblioteca de formulários. A interface **IMAPIFormMgr** permite que o cliente trabalhe com manipuladores de mensagens e execute resoluções entre classes de mensagens e bibliotecas de formulários. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg. cpp abre o Gerenciador de formulários para que um formulário possa ser selecionado.  <br/> |CMainDlg:: OnSelectForm  <br/> |MFCMAPI usa o método **MAPIOpenFormMgr** para abrir o Gerenciador de formulários para que um formulário possa ser selecionado.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

