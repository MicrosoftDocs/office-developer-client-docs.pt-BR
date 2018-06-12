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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 096437f10c5b992a1db55f6a856c38021a81b99a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767075"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**Aplica-se a**: Outlook 
  
Apresenta uma caixa de diálogo que permite ao usuário selecionar vários formulários e retorna uma matriz de formulário objetos de informações que descrevem esses formulários.
  
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

## <a name="parameters"></a>Par�metros

 _ulUIParam_
  
> [in] Uma alça para a janela pai da caixa de diálogo exibida. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres no passado. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _pszTitle_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém a legenda da caixa de diálogo. Se o parâmetro _pszTitle_ for NULL, o provedor de biblioteca de formulário que fornece os formulários fornece uma legenda padrão. 
    
 _pfld_
  
> [in] Um ponteiro para a pasta da qual selecionar os formulários. Se o parâmetro _pfld_ for NULL, os formulários são selecionados do contêiner formulário local, pessoal ou organização. 
    
 _pfrminfoarray_
  
> [in] Um ponteiro para uma matriz de objetos de informações de formulário que são pré-selecionados para o usuário.
    
 _ppfrminfoarray_
  
> [out] Um ponteiro para um ponteiro para a matriz retornada dos objetos de informações do formulário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo. 
    
## <a name="remarks"></a>Coment�rios

Visualizadores de formulário chame o método de **IMAPIFormMgr::SelectMultipleForms** para apresentado antes de uma caixa de diálogo que permite ao usuário selecionar vários formulários e, em seguida, para recuperar uma matriz de formulário informações objetos que descrevem os formulários selecionados. A caixa de diálogo **SelectMultipleForms** exibe todos os formulários, se ou não estão ocultos (ou seja, se ou não suas propriedades ocultas são criptografadas). 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Se um visualizador de formulário passa o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ , todas as cadeias de caracteres são Unicode. Provedores de biblioteca de formulário que não oferecem suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)

