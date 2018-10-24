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
ms.openlocfilehash: 6e8ea7230ae86dee99cc4413715055fc53afa900
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579722"
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
  
> [in] Um identificador para a janela pai do indicador de progresso é exibida enquanto o formulário é baixado. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MAPI_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o formulário é baixado. O seguinte sinalizador pode ser definido:
    
MAPI_DIALOG 
  
> Exibe uma interface de usuário para fornecer status ou solicita ao usuário para obter mais informações. Se esse sinalizador não estiver definida, nenhuma interface de usuário é exibida.
    
 _pfrmiInfo_
  
> [in] Um ponteiro para um objeto de informações de formulário para o formulário sejam baixados.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIFormMgr::PrepareForm** para baixar um formulário a partir de um contêiner de formulário para abertura. A maioria dos visualizadores de formulário não é necessário chamar **PrepareForm**, pois métodos [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) tanto o [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) chamam **PrepareForm**, se necessário. 
  
Você pode usar **PrepareForm** para obter as bibliotecas de vínculos dinâmicos (DLLs) e outros arquivos associados a um formulário para modificá-los. Se o formulário modificado for carregado de volta para seu contêiner de formulário, ele deve ser reinstalado. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

