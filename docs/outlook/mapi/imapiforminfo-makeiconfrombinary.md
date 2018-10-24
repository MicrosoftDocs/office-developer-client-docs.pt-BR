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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 30f55044327eecee3ab0d8ee2509d7132ab6e8ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570125"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um ícone de uma das propriedades ícone de um formulário se baseia.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Parâmetros

 _nPropID_
  
> [in] Um identificador de propriedade para uma propriedade de ícone.
    
 _phicon_
  
> [out] Um ponteiro para o ícone retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Aplicativos cliente chamam o método de **IMAPIFormInfo::MakeIconFromBinary** para criar um ícone de uma das propriedades ícone de um formulário. O parâmetro _nPropID_ , **MakeIconFromBinary** tira o identificador de propriedade de uma das propriedades ícone de um formulário. Usando esse identificador de propriedade, ele cria um ícone que pode ser exibido nos modos de exibição de tabela que incluem colunas de propriedade de ícones. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

