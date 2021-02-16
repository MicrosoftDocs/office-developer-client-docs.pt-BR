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
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413756"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Adicionado pelo Microsoft Excel sempre que o usuário ativa o XLL durante uma sessão do Excel usando o Add-In Manager. Essa função não é chamada quando o Excel é iniciado e carrega um complemento pré-instalado.
  
Essa função pode ser usada para exibir uma caixa de diálogo personalizada que informa ao usuário que o complemento foi ativado, para ler ou gravar no Registro, ou verificar informações de licenciamento, por exemplo.
  
O Excel não exige um XLL para implementar e exportar essa função.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não usa argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Sua implementação desta função deve retornar 1. (**int**).
  
## <a name="remarks"></a>Comentários

Use essa função se houver algo que seu XLL precise fazer quando for adicionado pelo Add-In Manager.
  
## <a name="example"></a>Exemplo

Veja  `\SAMPLES\EXAMPLE\EXAMPLE.C`  `\SAMPLES\GENERIC\GENERIC.C` e, por exemplo, implementações dessa função. O código a seguir é de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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

