---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f66d0fb1fc9d252ff8b6985c4a54de79313266d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577923"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Apresenta uma caixa de diálogo que permite que o usuário selecione um contêiner de formulário e retorna uma interface para o objeto de contêiner do usuário selecionado.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Uma alça para a janela pai da caixa de diálogo exibida. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a biblioteca de formulários está selecionada (ou seja, como o contêiner de formulário estiver selecionado). Sinalizadores a seguir podem ser definidos:
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> Pode ser feita a seleção de todos os contêineres. Este é o tipo de seleção padrão. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> Seleção pode ser feita apenas dos contêineres de pasta.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> Seleção pode ser feita apenas dos contêineres que não estão associados a pastas.
    
 _lppfcnt_
  
> [out] Um ponteiro para um ponteiro para a interface retornada. Esta interface é para o objeto de contêiner que está selecionado pelo usuário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário normalmente chame o método de **IMAPIFormMgr::SelectFormContainer** para selecionar um recipiente de formulário em que um formulário está instalado. **SelectFormContainer** não pode ser usado para selecionar o contêiner de formulário local, que tem o valor HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI usa o método **IMAPIFormMgr::SelectFormContainer** para selecionar um contêiner de formulário antes de renderizar seu conteúdo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

