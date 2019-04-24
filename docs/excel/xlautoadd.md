---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- função xlAutoAdd [Excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303987"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Adicionado pelo Microsoft Excel sempre que o usuário ativa o XLL durante uma sessão do Excel usando o Gerenciador de suplementos. Esta função não é chamada quando o Excel é iniciado e carrega um suplemento pré-instalado.
  
Essa função pode ser usada para exibir uma caixa de diálogo personalizada que informa ao usuário que o suplemento foi ativado, ou para ler ou gravar no registro, ou verificar informações de licenciamento, por exemplo.
  
O Excel não requer um XLL para implementar e exportar essa função.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não usa argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Sua implementação dessa função deve retornar 1. (**int**).
  
## <a name="remarks"></a>Comentários

Use essa função se houver alguma coisa que o seu XLL precisa fazer quando for adicionado pelo Gerenciador de suplementos.
  
## <a name="example"></a>Exemplo

Consulte `\SAMPLES\EXAMPLE\EXAMPLE.C` e `\SAMPLES\GENERIC\GENERIC.C` , por exemplo, implementações dessa função. O código a seguir é de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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


[Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

