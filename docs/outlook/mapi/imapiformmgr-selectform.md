---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b481eaf00b7568da5f02ffa3301e8f2698a98e1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767059"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**Aplica-se a**: Outlook 
  
Apresenta uma caixa de diálogo que permite que o usuário selecione um formulário e retorna um objeto de informações de formulário que descreve nesse formulário.
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Uma alça para a janela pai da caixa de diálogo exibida. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres no passado. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _pszTitle_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém a legenda da caixa de diálogo. Se o parâmetro _pszTitle_ for NULL, o provedor de biblioteca de formulário fornece uma legenda padrão. 
    
 _pfld_
  
> [in] Um ponteiro para a pasta da qual selecionar o formulário. Se o parâmetro _pfld_ for NULL, o formulário pode ser selecionado do contêiner formulário local, pessoal ou organização. 
    
 _ppfrminfoReturned_
  
> [out] Um ponteiro para um ponteiro para o objeto de informações do formulário retornado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIFormMgr::SelectForm** para presente primeiro uma caixa de diálogo que permite que o usuário selecione um formulário e, em seguida, para recuperar um objeto de informações do formulário que descreve o formulário selecionado. A caixa de diálogo restringe o usuário selecione um formulário simples. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A caixa de diálogo **SelectForm** exibe somente os formulários que não estão ocultos (ou seja, formulários que têm as suas propriedades ocultas limpar). Se um visualizador de formulário passa o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ , todas as cadeias de caracteres são Unicode. Provedores de biblioteca de formulário que não oferecem suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI usa o método **IMAPIFormMgr::SelectForm** para selecionar um formulário e enviar informações sobre o formulário para um ou mais logs.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

