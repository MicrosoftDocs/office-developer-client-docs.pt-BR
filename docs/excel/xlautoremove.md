---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- Função xlautoremove [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425474"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chamado pelo Microsoft Excel sempre que o usuário desativa o XLL durante uma sessão do Excel usando o Add-In Manager. Esta função não é chamada quando uma sessão do Excel é fechada, normalmente ou de forma anormal, com o suplemento instalado.
  
Essa função pode ser usada para exibir uma caixa de diálogo personalizada que diz ao usuário que o complemento foi desativado ou para ler ou gravar no Registro, por exemplo.
  
O Excel não exige um XLL para implementar e exportar essa função. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não usa argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A implementação dessa função deve retornar 1 (**int**).
  
## <a name="remarks"></a>Comentários

Use essa função se o XLL precisar concluir qualquer tarefa quando ela for removida pelo Add-In Manager.
  
## <a name="example"></a>Exemplo

Veja os arquivos `\SAMPLES\EXAMPLE\EXAMPLE.C` e `\SAMPLES\GENERIC\GENERIC.C` como exemplos de implementações dessa função. O código a seguir é de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a>Confira também



[xlAutoAdd](xlautoadd.md)


[Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

