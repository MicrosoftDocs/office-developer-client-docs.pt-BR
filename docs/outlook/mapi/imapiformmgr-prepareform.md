---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416647"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Baixa um formulário para abertura.
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> no Uma alça para a janela pai do indicador de progresso que é exibida enquanto o formulário é baixado. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o formulário é baixado. O seguinte sinalizador pode ser definido:
    
MAPI_DIALOG 
  
> Exibe uma interface do usuário para fornecer status ou solicitar mais informações ao usuário. Se esse sinalizador não for definido, nenhuma interface de usuário será exibida.
    
 _pfrmiInfo_
  
> no Um ponteiro para um objeto de informações de formulário para o formulário ser baixado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormMgr::P repareform** para baixar um formulário de um contêiner de formulários para abertura. A maioria dos visualizadores de formulário não precisa chamar **PrepareForm**, porque os métodos [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) e [IMAPIFormMgr:: loadform](imapiformmgr-loadform.md) chamam **PrepareForm**, se necessário. 
  
Você pode usar o **PrepareForm** para obter as bibliotecas de vínculo dinâmico (DLLs) e outros arquivos associados a um formulário para modificá-los. Se o formulário modificado for carregado de volta para o contêiner de formulários, ele deverá ser reinstalado. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

