---
title: Compatibilidade com versões anteriores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilidade de versão [excel 2007,] compatibilidade XLL [Excel 2007], [Excel 2007] compatibilidade com versões anteriores
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301677"
---
# <a name="backward-compatibility"></a>Compatibilidade com versões anteriores

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Este tópico aborda os problemas de compatibilidade XLL em diferentes versões do Microsoft Excel.
  
## <a name="useful-constant-definitions"></a>Definições de constantes úteis

Considere incluir definições semelhantes a esses elementos no seu código do project XLL e substituir todas as instâncias de números literais usadas neste contexto. Isso irá esclarecer o código específicos da versão e reduzir a probabilidade de bugs relacionados à versão no formulário de números de aparência inofensiva.
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a>Obter a versão em execução

Você deve detectar qual versão está sendo executada usando `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, que é `arg` uma definição numérico **XLOPER** como o 2. A versão é uma cadeia de caracteres **XLOPER** que pode ser forçada a um numérico inteiro. Para o Microsoft Excel 2013, ele é 15.0. Fazer isso em ou a partir da função, [xlAutoOpen](xlautoopen.md). Em seguida, você pode definir uma variável global que informe todos os módulos do seu projeto em que a versão do Excel está em execução. O código pode decidir se vai acionar usando a API C **Excel12** e **XLOPER12** s ou usando **Excel4** usando **XLOPER** s.
  
Você pode acionar **XLCallVer** para descobrir a versão API C, mas isso não indica qual das versões anteriores do Excel 2007 você está executando. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Criar suplementos que exportam interfaces duplas

Considere uma função XLL que leva de uma cadeia de caracteres e retorna um valor que pode ser qualquer um dos tipos de dados de planilha. Você pode exportar uma função registrada como tipo PD e com o protótipo a seguir, onde a cadeia é passada como uma cadeia de comprimento contados em bytes. 
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Embora isso funcione muito bem, há vários motivos para que ela não seja a interface ideal para o código a partir do Excel 2007:
  
- Ele está sujeito às limitações de cadeias de caracteres de bytes C API e não é possível acessar as longas cadeias de caracteres Unicode com suporte a partir do Excel 2007.
    
- No entanto, a partir do Excel 2007, o Excel pode passar e aceitar o **XLOPER** s. Internamente ele os converte para **XLOPER12** s. Portanto, há uma conversão implícita de sobrecarga a partir do Excel 2007 que não estará lá quando o código for executado em versões anteriores do Excel.
    
- Talvez esta função possa ser feita com thread de segurança, mas se a cadeia de caracteres é alterada para `PD$`, o registro falhará em Iniciar antes do Excel 2007.
    
Por esse motivo, idealmente, a partir do Excel 2007, você deve exportar uma função para os usuários que foram registrado como `QD%$`, supondo que o código tenha thread de segurança, como no protótipo a seguir.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Outro motivo, para que você querer registrar uma função diferente a partir do Excel 2007 é o fato das funções XLL permitir acima de 255 argumentos, em vez do limite de 30 das versões anteriores.
  
Felizmente, você pode ter os benefícios de ambos ao exportar as duas versões do seu projeto. Você pode detectar a versão do Excel em execução e inscrever condicionalmente a função mais apropriada. Para mais informações e para um exemplo de implementação, confira [desenvolvendo suplementos (XLLs) no Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).
  
Essa abordagem traz a possibilidade de uma planilha em execução no Excel 2003 poder exibir resultados diferentes do que a execução da mesma planilha a partir do Excel 2007. Por exemplo, o Excel 2003 mapearia uma cadeia Unicode em uma célula de planilha do Excel 2003 para uma cadeia de bytes ASCII e truncaria antes de passar para uma função XLL. A partir do Excel 2007, o Excel passará uma cadeia Unicode não convertida para uma função XLL registrada da maneira certa. Isso pode levar a um resultado diferente. Você deve estar ciente dessa possibilidade e das consequências aos seus usuários, não apenas na atualização. Por exemplo, algumas funções internas numéricas foram aprimoradas entre o Excel 2003 e o Excel 2000.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Novas funções de planilha e funções de análise

Funções de análise de ferramentas (ATP) fazem parte do Excel a partir do Excel 2007. Anteriormente, um XLL apenas poderia acionar uma função ATP usando [xlUDF](xludf.md). A partir do Excel 2007, funções ATP devem ser acionadas usando enumerações de função estipuladas em xlcall. h. O exemplo em Chamar funções definidas pelo usuário a partir de DLLs demonstra dois métodos diferentes.
  
## <a name="see-also"></a>Confira também

- [Retorno de chamada da API de C: funções Excel4, Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programação com a API de C no Excel](programming-with-the-c-api-in-excel.md)
- [Novidades na API de C do Excel](what-s-new-in-the-c-api-for-excel.md)

