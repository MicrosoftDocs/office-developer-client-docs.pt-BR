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
ms.openlocfilehash: ed3f793e4353cf78949a9df3a17dd3997a573f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767044"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**Aplica-se a**: Outlook 
  
Abre um formulário para criar uma nova mensagem, com base na classe de mensagem do formulário.
  
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
  
> [in] Uma alça para a janela pai para o indicador de progresso é exibida enquanto o formulário é aberto. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o formulário é aberto. O seguinte sinalizador pode ser definido:
    
MAPI_DIALOG 
  
> Exibe uma interface de usuário para fornecer status ou solicita ao usuário para obter mais informações. Se esse sinalizador não estiver definida, nenhuma interface de usuário é exibida.
    
 _pfrminfoToActivate_
  
> [in] Um ponteiro para o objeto de informações do formulário que é usado para abrir o formulário.
    
 _refiidToAsk_
  
> [in] Um ponteiro para o identificador de interface (IID) para a interface a ser retornado para o objeto de formulário que foi criado. O parâmetro _refiidToAsk_ não deve ser NULL. 
    
 _ppvObj_
  
> [out] Um ponteiro para um ponteiro para a interface retornada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_NO_INTERFACE 
  
> Não há suporte para a interface solicitada pelo objeto form.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método **IMAPIFormMgr::CreateForm** para abrir um formulário para criar uma nova mensagem, com base na classe de mensagem do formulário. **CreateForm** abre o formulário criando uma instância do servidor de formulário para nesse formulário, conforme descrito no objeto informações determinado formulário. Se for necessário, **CreateForm** chama o método [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) para baixar o código de servidor do formulário no disco do usuário. 
  
O parâmetro _pfrminfoToActivate_ deve apontar para um objeto de informações de formulário que foi resolvido corretamente. 
  
Depois que o formulário foi aberto, a tela de formulário a chamada deve configurar uma mensagem usando a interface [IPersistMessage](ipersistmessageiunknown.md) e, opcionalmente, pode configurar um contexto de modo de exibição para o formulário. Para obter mais informações, consulte [Lançar um servidor do formulário](launching-a-form-server.md). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI usa o método **IMAPIFormMgr::CreateForm** para criar um formulário antes exibi-las.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Iniciar um servidor de formulário](launching-a-form-server.md)

