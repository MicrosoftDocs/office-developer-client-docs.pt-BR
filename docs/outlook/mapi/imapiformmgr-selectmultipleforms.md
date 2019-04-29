---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c40d853c49645638c2ec4001d86e64a1b2d2e381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420308"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Apresenta uma caixa de diálogo que permite ao usuário selecionar vários formulários e retorna uma matriz de objetos de informações de formulário que descrevem esses formulários.
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> no Uma alça para a janela pai da caixa de diálogo exibida. 
    
 _ulFlags_
  
> no Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 _pszTitle_
  
> no Um ponteiro para uma cadeia de caracteres que contém a legenda da caixa de diálogo. Se o parâmetro _pszTitle_ for NULL, o provedor de biblioteca de formulários que fornecerá os formulários fornecerá uma legenda padrão. 
    
 _pfld_
  
> no Um ponteiro para a pasta da qual os formulários serão selecionados. Se o parâmetro _pfld_ for NULL, os formulários serão selecionados do contêiner de formulário local, pessoal ou organização. 
    
 _pfrminfoarray_
  
> no Um ponteiro para uma matriz de objetos de informações de formulário que são preselecionadas para o usuário.
    
 _ppfrminfoarray_
  
> bota Um ponteiro para um ponteiro para a matriz retornada de objetos de informação do formulário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormMgr:: SelectMultipleForms** para primeiro apresentar uma caixa de diálogo que permite ao usuário selecionar vários formulários e, em seguida, recuperar uma matriz de objetos de informações de formulário que descrevem os formulários selecionados. A caixa de diálogo **SelectMultipleForms** exibe todos os formulários, independentemente de estarem ou não ocultos (ou seja, se suas propriedades ocultas estão desmarcadas ou não). 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se um visualizador de formulários passar o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ , todas as cadeias de caracteres serão Unicode. Os provedores de biblioteca de formulários que não dão suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

