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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405111"
---
# <a name="imapiforminfomakeiconfrombinary"></a>IMAPIFormInfo::MakeIconFromBinary

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um ícone a partir de uma das propriedades de ícone de um formulário.
  
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
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam o método **IMAPIFormInfo::MakeIconFromBinary** para criar um ícone a partir de uma das propriedades de ícone de um formulário. No parâmetro  _nPropID,_ **MakeIconFromBinary** assume o identificador de propriedade de uma das propriedades de ícone de um formulário. Usando esse identificador de propriedade, ele cria um ícone que pode ser exibido em exibições de tabela que incluem colunas de propriedade para ícones. 
  
## <a name="see-also"></a>Confira também



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

