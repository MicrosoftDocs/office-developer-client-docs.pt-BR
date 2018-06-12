---
title: Compatibilidade com versões anteriores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilidade de versão [excel 2007], compatibilidade XLL [Excel 2007], [Excel 2007] de compatibilidade com versões anteriores
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 095961fa909a67b354ed43a7e093b79a9ebb4f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765263"
---
# <a name="backward-compatibility"></a>Compatibilidade com versões anteriores

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Este tópico aborda os problemas de compatibilidade XLL em versões diferentes do Microsoft Excel.
  
## <a name="useful-constant-definitions"></a>Definições constantes úteis

Considere incluindo definições semelhantes a estas em seu código de projeto XLL e substituindo todas as instâncias de números literais usadas nesse contexto. Isso esclarecer o código que é específico de versão e reduzir a probabilidade de bugs relacionados à versão no formato dos números inofensiva.
  
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

## <a name="getting-the-running-version"></a>Obtendo a versão em execução

Você deve detectar qual versão está sendo executado usando `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, onde `arg` é um **XLOPER** numérico definido como 2 e versão é uma cadeia de caracteres **XLOPER** , que então pode ser forçada como um número inteiro. Para o Microsoft Excel 2013, isso é 15.0. Você deve fazer isso em ou a função [xlAutoOpen](xlautoopen.md) de. Em seguida, você pode definir uma variável global que informa que todos os módulos no seu projeto do qual versão do Excel está sendo executado. Seu código, em seguida, poderá decidir se chame o API C usando **Excel12** e **XLOPER12**s ou **Excel4** usando **XLOPER**s.
  
Você pode chamar **XLCallVer** para descobrir a versão do C API, mas isso não indica qual das versões anteriores do Excel 2007 você está executando. 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a>Criando suplementos que exportam interfaces duplas

Considere uma função XLL que utiliza uma cadeia de caracteres e retorna um valor que pode ser qualquer um dos tipos de dados de planilha. Você pode exportar uma função registrada conforme digita "PD" e com protótipo da seguinte maneira em que a cadeia de caracteres é passada como uma cadeia de caracteres de byte de comprimento contado.
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
Embora isso funcione perfeitamente bem, há vários motivos por que isso não é a interface ideal para seu código iniciando no Excel 2007:
  
- Ela está sujeito às limitações de cadeias de caracteres de byte C API e não pode acessar as Unicode cadeias de caracteres longas suportadas iniciada no Excel 2007.
    
- Embora, começando no Excel 2007, Excel pode passar e aceitar **XLOPER**s, internamente ele os converte em **XLOPER12**s, portanto, há uma sobrecarga de conversão implícita iniciada no Excel 2007 que não existe quando o código é executado em versões anteriores do Excel.
    
- Pode ser que esta função pode ser feita segmento seguros, mas se o tipo de cadeia de caracteres for alterado para `PD$`, registro falha na inicialização antes do Excel 2007.
    
Por esses motivos, idealmente, iniciando no Excel 2007, você deve exportar uma função para os usuários que foi registrado como `QD%$`, assumindo que seu código é thread segura e com protótipo da seguinte maneira.
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
Outro motivo por que talvez você queira registrar uma função diferente iniciando no Excel 2007 é que ele permite que funções XLL assumam até 255 argumentos, em vez do limite de 30 de versões anteriores.
  
Felizmente, é possível ter os benefícios de ambas exportando as duas versões do projeto. Você pode detectar, em seguida, a versão do Excel em execução e condicionalmente, registra a função mais apropriada. Para obter mais informações e um exemplo de implementação, consulte [Developing suplementos (XLLs) no Excel 2007](http://msdn.microsoft.com/en-us/library/aa730920.aspx).
  
Essa abordagem leva à possibilidade de que uma planilha executada no Excel 2003 poderia exibir resultados diferentes da mesma planilha executando iniciada no Excel 2007. Por exemplo, o Excel 2003 seria mapear uma cadeia de caracteres Unicode em uma célula de planilha do Excel 2003 para uma sequência de byte ASCII e truncá-lo antes de passá-la para uma função XLL. Iniciando no Excel 2007, Excel passará uma sequência de caracteres Unicode não convertida para uma função XLL registrada da forma correta. Isso pode implicar um resultado diferente. Você deve estar ciente dessa possibilidade e as consequências para seus usuários, não apenas na atualização. Por exemplo, algumas funções numéricas internas foram aperfeiçoadas entre o Excel 2000 e o Excel 2003.
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a>Novas funções de planilha e ferramentas de análise

Funções do análise (ATP) de ferramentas fazem parte do Excel iniciada no Excel 2007. Anteriormente, um XLL somente poderia chamar uma função ATP usando [xlUDF](xludf.md). Iniciando no Excel 2007, as funções ATP devem ser chamadas usando as enumerações de função definidas no xlcall. h. O exemplo em funções definidas pelo usuário chamando a partir de DLLs demonstra os dois métodos diferentes.
  
## <a name="see-also"></a>Confira também

- [C API Callback Functions Excel4, Excel12](c-api-callback-functions-excel4-excel12.md) 
- [Programando com a API C no Excel](programming-with-the-c-api-in-excel.md)
- [What's New in the C API for Excel](what-s-new-in-the-c-api-for-excel.md)

