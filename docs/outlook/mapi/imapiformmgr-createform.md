---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419846"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre um formulário para criar uma nova mensagem com base na classe de mensagem do formulário.
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> no Uma alça para a janela pai do indicador de progresso que é exibido enquanto o formulário é aberto. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o formulário é aberto. O seguinte sinalizador pode ser definido:
    
MAPI_DIALOG 
  
> Exibe uma interface do usuário para fornecer status ou solicitar mais informações ao usuário. Se esse sinalizador não for definido, nenhuma interface de usuário será exibida.
    
 _pfrminfoToActivate_
  
> no Um ponteiro para o objeto de informações do formulário que é usado para abrir o formulário.
    
 _refiidToAsk_
  
> no Um ponteiro para o identificador de interface (IID) da interface a ser retornado para o objeto Form que foi criado. O parâmetro _refiidToAsk_ não deve ser nulo. 
    
 _ppvObj_
  
> bota Um ponteiro para um ponteiro para a interface retornada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NO_INTERFACE 
  
> A interface solicitada não é suportada pelo objeto Form.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormMgr:: CreateForm** para abrir um formulário para criar uma nova mensagem com base na classe de mensagem do formulário. **CreateForm** abre o formulário criando uma instância do servidor de formulário para esse formulário, conforme descrito no objeto de informações do formulário determinado. Se necessário, **CreateForm** chama o método [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) para baixar o código do servidor de formulário no disco do usuário. 
  
O parâmetro _pfrminfoToActivate_ deve apontar para um objeto de informações de formulário que foi resolvido corretamente. 
  
Depois que o formulário é aberto, o Visualizador de formulário de chamada deve configurar uma mensagem usando a interface [IPersistMessage](ipersistmessageiunknown.md) e, opcionalmente, pode configurar um contexto de exibição para o formulário. Para obter mais informações, consulte [iniciando um servidor de formulários](launching-a-form-server.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI usa o método **IMAPIFormMgr:: CreateForm** para criar um formulário antes de exibi-lo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Iniciar um servidor de formulário](launching-a-form-server.md)

