---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a230e8b69a64646dffb23147345d5960fdd38581
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767034"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Aplica-se a**: Outlook 
  
Um ícone de uma das propriedades ícone de um formulário se baseia.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Par�metros

 _nPropID_
  
> [in] Um identificador de propriedade para uma propriedade de ícone.
    
 _phicon_
  
> [out] Um ponteiro para o ícone retornado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Coment�rios

Aplicativos cliente chamam o método de **IMAPIFormInfo::MakeIconFromBinary** para criar um ícone de uma das propriedades ícone de um formulário. O parâmetro _nPropID_ , **MakeIconFromBinary** tira o identificador de propriedade de uma das propriedades ícone de um formulário. Usando esse identificador de propriedade, ele cria um ícone que pode ser exibido nos modos de exibição de tabela que incluem colunas de propriedade de ícones. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)

