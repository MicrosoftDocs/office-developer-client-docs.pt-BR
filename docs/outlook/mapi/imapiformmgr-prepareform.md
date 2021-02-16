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
  
> [in] Um alça para a janela pai do indicador de progresso que é exibido enquanto o formulário é baixado. O _parâmetro ulUIParam é ignorado,_ a menos que o MAPI_DIALOG padrão seja definido no _parâmetro ulFlags._ 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o formulário é baixado. O sinalizador a seguir pode ser definido:
    
MAPI_DIALOG 
  
> Exibe uma interface do usuário para fornecer status ou solicitar ao usuário mais informações. Se esse sinalizador não estiver definido, nenhuma interface do usuário será exibida.
    
 _pfrmiInfo_
  
> [in] Um ponteiro para um objeto de informações de formulário para o formulário a ser baixado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam **o método IMAPIFormMgr::P repareForm** para baixar um formulário de um contêiner de formulário para abertura. A maioria dos visualizadores de formulário não precisa chamar **PrepareForm**, porque os métodos [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) e [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) chamam **PrepareForm,** se necessário. 
  
Você pode usar **o PrepareForm** para obter as bibliotecas de vínculo dinâmico (DLLs) e outros arquivos associados a um formulário para modificá-los. Se o formulário modificado for carregado de volta em seu contêiner de formulário, ele deverá ser reinstalado. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

