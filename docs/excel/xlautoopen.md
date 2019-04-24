---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- função xlAutoOpen [Excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310287"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de retorno de chamada que deve ser implementada e exportada por cada XLL válido. A função **xlAutoOpen** é o local recomendado de onde registrar funções e comandos XLL, inicializar estruturas de dados, personalizar a interface do usuário e assim por diante. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não usa argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A implementação dessa função deve retornar 1 (**int**).
  
## <a name="remarks"></a>Comentários

O Microsoft Excel chama **xlAutoOpen** sempre que o XLL é ativado. O XLL é ativado nas seguintes situações: 
  
- No início de uma sessão do Excel, se ela estiver ativa na última sessão do Excel que terminou normalmente.
    
- Se carregado durante uma sessão do Excel.
    
- Um XLL pode ser carregado de várias maneiras:
    
- Escolhendo **abrir** no menu **arquivo** (onde a versão do Excel dá suporte a esse método de carregamento de XLLs). 
    
- Usando o Gerenciador de Suplemento.
    
- De outro XLL que chama [xlfRegister](xlfregister-form-1.md) com o nome dessa DLL como o único argumento. 
    
- De uma planilha de macro XLM que chama [Register](xlfregister-form-1.md) com o nome dessa DLL como o único argumento. 
    
- Se o suplemento for desativado e reativado durante uma sessão do Excel, essa função será chamada na reativação.
    
### <a name="example"></a>Exemplo

Consulte os arquivos `SAMPLES\EXAMPLE\EXAMPLE.C` e `SAMPLES\GENERIC\GENERIC.C`, e, por exemplo, implementações dessa função.
  
## <a name="see-also"></a>Confira também



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

