---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- função xlautoadd [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ae0b4ae2d5f5fc58c3e18ffa9d79ec4128cb4639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765448"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Adicionado pelo Microsoft Excel sempre que o usuário ativa o XLL durante uma sessão do Excel usando o Gerenciador de suplemento. Essa função não é chamada quando o Excel é iniciado e carrega um suplemento pré-instaladas.
  
Esta função pode ser usada para exibir uma caixa de diálogo personalizada que informa ao usuário que o suplemento tiver sido ativado, ou para ler ou gravar no registro ou verificar as informações de licenciamento, por exemplo.
  
Excel não exige um XLL implementar e exportar essa função.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Par�metros

Essa função não assume nenhum argumento.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

A implementação dessa função deve retornar 1. (**int**).
  
## <a name="remarks"></a>Coment�rios

Use esta função se não houver nada que seu XLL precisa fazer quando ele é adicionado pelo gerente de suplemento.
  
## <a name="example"></a>Example

Consulte `\SAMPLES\EXAMPLE\EXAMPLE.C` e `\SAMPLES\GENERIC\GENERIC.C` por exemplo implementações dessa função. O código a seguir é de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a>Confira também



[xlAutoRemove](xlautoremove.md)


[Gerenciador de suplemento e funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

