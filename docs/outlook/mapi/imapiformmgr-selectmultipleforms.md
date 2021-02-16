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
  
> [in] Um alça para a janela pai da caixa de diálogo exibida. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _pszTitle_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém a legenda da caixa de diálogo. Se o  _parâmetro pszTitle_ for NULL, o provedor da biblioteca de formulários que fornece os formulários fornece uma legenda padrão. 
    
 _pfld_
  
> [in] Um ponteiro para a pasta a partir da qual os formulários são selecionados. Se o  _parâmetro pfld_ for NULL, os formulários serão selecionados no contêiner de formulário local, pessoal ou da organização. 
    
 _pfrminfoarray_
  
> [in] Um ponteiro para uma matriz de objetos de informações de formulário que são pré-selecionados para o usuário.
    
 _ppfrminfoarray_
  
> [out] Um ponteiro para um ponteiro para a matriz retornada de objetos de informações de formulário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão **Cancelar** na caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam o método **IMAPIFormMgr::SelectMultipleForms** para apresentar primeiro uma caixa de diálogo que permite ao usuário selecionar vários formulários e, em seguida, recuperar uma matriz de objetos de informações de formulário que descrevem os formulários selecionados. A **caixa de diálogo SelectMultipleForms** exibe todos os formulários, se eles estão ocultos ou não (ou seja, se suas propriedades ocultas são claras ou não). 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se um visualizador de formulário passar o sinalizador MAPI_UNICODE no  _parâmetro ulFlags,_ todas as cadeias de caracteres serão Unicode. Provedores de biblioteca de formulário que não suportam cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE for passado. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

