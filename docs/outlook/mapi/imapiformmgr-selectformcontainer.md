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
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428589"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Apresenta uma caixa de diálogo que permite ao usuário selecionar um contêiner de formulário e retorna uma interface para o objeto contêiner selecionado pelo usuário.
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um alça para a janela pai da caixa de diálogo exibida. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a biblioteca de formulário é selecionada (ou seja, como o contêiner de formulário é selecionado). Os sinalizadores a seguir podem ser definidos:
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> A seleção pode ser feita de todos os contêineres. Esse é o tipo de seleção padrão. 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> A seleção só pode ser feita a partir de contêineres de pasta.
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> A seleção só pode ser feita de contêineres que não estão associados a pastas.
    
 _lppfcnt_
  
> [out] Um ponteiro para um ponteiro para a interface retornada. Essa interface é para o objeto de contêiner selecionado pelo usuário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário normalmente chamam o método **IMAPIFormMgr::SelectFormContainer** para selecionar um contêiner de formulário no qual um formulário está instalado. **SelectFormContainer** não pode ser usado para selecionar o contêiner de formulário local, que tem o valor HFRMREG_LOCAL. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI usa o **método IMAPIFormMgr::SelectFormContainer** para selecionar um contêiner de formulário antes de renderizar seu conteúdo.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

