---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- função xlautoremove [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 6e5daac21a6d89472a7d84a25e9aeaea56db1ae1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765466"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chamado pelo Microsoft Excel sempre que o usuário desativa o XLL durante uma sessão do Excel usando o Gerenciador de suplemento. Essa função não é chamada quando uma sessão do Excel é fechado, normalmente ou modo anormal, com o suplemento instalado.
  
Esta função pode ser usada para exibir uma caixa de diálogo personalizada informando ao usuário que o suplemento foi desativado, ou para ler ou gravar no registro, por exemplo.
  
Excel não exige um XLL implementar e exportar essa função. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Par�metros

Essa função não assume nenhum argumento.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

A implementação dessa função deve retornar 1 (**int**).
  
## <a name="remarks"></a>Coment�rios

Use esta função se seu XLL precisa concluir qualquer tarefa quando ele é removido pelo gerente de suplemento.
  
## <a name="example"></a>Example

Consulte os arquivos `\SAMPLES\EXAMPLE\EXAMPLE.C` e `\SAMPLES\GENERIC\GENERIC.C` por exemplo implementações dessa função. O código a seguir é de `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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


[Gerenciador de suplemento e funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

