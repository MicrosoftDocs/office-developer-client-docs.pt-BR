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
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342109"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um ícone com base em uma das propriedades de ícone de um formulário.
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a>Parâmetros

 _nPropID_
  
> no Um identificador de propriedade para uma Propriedade Icon.
    
 _phicon_
  
> bota Um ponteiro para o ícone retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam o método **IMAPIFormInfo:: MakeIconFromBinary** para criar um ícone de uma das propriedades de ícone de um formulário. No parâmetro _nPropID_ , **MakeIconFromBinary** Obtém o identificador de propriedade de uma das propriedades de ícone de um formulário. Usando esse identificador de propriedade, ele cria um ícone que pode ser exibido em modos de exibição de tabela que incluem colunas de propriedade para ícones. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

