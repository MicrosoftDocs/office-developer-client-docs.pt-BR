---
title: Formatos numéricos personalizados da função Format (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 97efe972-d873-47d7-be81-8ae3461870c4
description: Saiba como controlar como um número é exibido criando um formato de número definido pelo usuário
ms.openlocfilehash: fac128ce13edf89105fbee7319533e1a3f346d05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765093"
---
# <a name="custom-numeric-formats-for-the-format-function-access-custom-web-app"></a>Formatos numéricos personalizados da função Format (aplicativo Web personalizado do Access)

Saiba como controlar como um número é exibido criando um formato de número definido pelo usuário
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-BR/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 

Você pode alterar a maneira como um número é exibido criando um formato de número definido pelo usuário. Um formato de número definido pelo usuário pode conter de uma a três seções separadas por um ponto e vírgula (;). Se o argumento Style da função [Função Format (aplicativo Web personalizado do Access)](format-function-access-custom-web-app.md) contiver um dos formatos numéricos predefinidos, somente uma seção será permitida. 
  
## <a name="format-specifications"></a>Especificações de formato
<a name="bk_addresources"> </a>

A tabela a seguir lista os caracteres que você pode usar para criar formatos de número definidos pelo usuário.
  
|**Especificação de formato**|**Descrição**|
|:-----|:-----|
|Nenhum  <br/> |Exibe o número sem formatação.  <br/> |
|**0** (caractere zero)  <br/> |Espaço reservado de dígito. Exibe um dígito ou um zero. Se a expressão tiver um dígito na posição onde o zero aparece na cadeia de caracteres de formato, exibe o dígito; caso contrário, exibe um zero nessa posição.  <br/> Se o número tiver menos dígitos do que zeros (em qualquer casa decimal) na expressão de formato, exibe os zeros à esquerda ou à direita. Se o número tiver mais dígitos do que zeros ao lado direito do separador de decimais na expressão de formato, arredonda o número de casas decimais de acordo com o número de zeros. Se o número tiver mais dígitos do que zeros à esquerda do separador de decimais na expressão de formato, exibe os dígitos adicionais sem modificação.  <br/> |
|#  <br/> |Espaço reservado de dígito. Exibe um dígito ou nada. Se a expressão tiver um dígito na posição onde o caractere # aparece na cadeia de caracteres de formato, exibe o dígito; caso contrário, não exibe nada nessa posição.  <br/> Este símbolo funciona exatamente como o espaço reservado de dígito 0, excetuando que os zeros à esquerda e à direita não são exibidos caso o número tenha menos dígitos do que caracteres # em cada lado do separador de decimais na expressão de formato.  <br/> |
|. (caractere de ponto)  <br/> |Espaço reservado de decimal. O espaço reservado de decimal determina quantos dígitos são exibidos à esquerda e à direita do separador de decimais. Se a expressão de formato contiver somente # caracteres à esquerda deste símbolo, os números menores do que 1 começam com um separador de decimais. Para exibir um zero à esquerda com números fracionados, use zero como o espaço reservado de primeiro dígito à esquerda do separador de decimais. Em alguns locais, uma vírgula é usada como o separador de decimais. O caractere atual que é usado como um espaço reservado de decimais na saída formatada depende do formato de número reconhecido pelo sistema. Por isso, você deveria usar o ponto como caractere de espaço reservado de decimais nos seus formatos mesmo caso esteja num local que use vírgulas para essa função. A cadeia de caracteres formatada será exibida no formato correto para o local.  <br/> |
|%  <br/> |Espaço reservado de porcentagem. Multiplica a expressão por 100. O caractere de porcentagem (%) é inserido na posição onde aparece na cadeia de caracteres de formato.  <br/> |
|, (caractere de vírgula)  <br/> |Separador de milhar. O separador de milhar separa os milhares das centenas em um número que tenha quatro ou mais posições à esquerda do separador de decimais. O uso padrão do separador de milhar é especificado se o formato contiver um separador de milhar anexado nos espaços reservados de dígito (0 ou #).  <br/> Usar um separador de milhar imediatamente à esquerda do separador de decimais (se uma casa decimal estiver especificada) ou como o caractere mais à direita na cadeia de caracteres significa "ajustar escala do número dividindo-o por 1.000, arredondando conforme necessário". Números menores do que 1.000 mas maiores ou iguais a 500 são exibidos como 1, e números menores que 500 são exibidos como 0. Dois separadores de milhar adjacentes nesta posição ajustam a escala por um fator de 1 milhão, e um fator adicional de 1.000 por cada separador adicional.  <br/> Múltiplos separadores em qualquer posição que não imediatamente à esquerda do separador de decimais ou na posição mais à direita da cadeia de caracteres são tratados somente para especificar o uso de um separador de milhar. Em alguns locais, um ponto é usado como separador de milhar. O caractere real que é usado como separador de milhar na saída formatada depende do Formato de Número reconhecido pelo sistema. Por isso, você deve usar a vírgula como separador de milhar nos seus formatos, mesmo caso esteja num local que use vírgulas para essa função. A cadeia de caracteres formatada será exibida no formato correto para o local.  <br/> Por exemplo, considere as três cadeias de caractere de formato seguintes:  <br/> "#,0.", que usa o separador de milhar para formatar o número 100 milhões como a cadeia de caracteres "100.000.000".  <br/> "#0,.", que ajusta a escala em um fator de um milhar, para formatar o número 100 milhões como a cadeia de caracteres "100000".  <br/> "#,0,.", que usa o separador de milhar e ajusta a escala por um milhar para formatar o número 100 milhões como a cadeia de caracteres "100.000".  <br/> |
|: (caractere de dois pontos)  <br/> |Separador de tempo. Em alguns locais, outros caracteres podem ser usados para representar o separador de tempo. O separador de tempo separa as horas, minutos e segundos ao formatar valores de tempo. O caractere real usado como separador de tempo na saída formatada é determinado pelas configurações do sistema.  <br/> |
|/ (caractere de barra para a frente)  <br/> |Separador de data. Em alguns locais, outros caracteres podem ser usados para representar o separador de data. O separador de data separa o dia, mês e ano ao formatar valores de data. O caractere real usado como separador de data na saída formatada é determinado pelas configurações do sistema.  <br/> |
|**E- , E+ , e- , e+** <br/> |Formato científico. Se a expressão de formato contiver pelo menos um espaço reservado de dígito (0 ou #) à esquerda do E-, E+, e-, ou e+, o número é exibido em formato científico e E ou e são inseridos entre o número e o seu expoente. O número de espaços reservados de dígito à esquerda determinam o número de dígitos no expoente. Use E- ou e- para posicionar um símbolo de menos próximo a expoentes negativos. Use E+ ou e+ para posicionar um símbolo de menos próximo a expoentes negativos e um símbolo de mais próximo a expoentes positivos. Você também deve incluir os espaços reservados de dígito à direita deste símbolo para obter a formatação correta.  <br/> |
|**- + $ ( )** <br/> |Caracteres literais. Estes caracteres são exibidos exatamente como digitados na cadeia de caracteres de formato. Para exibir outro caractere que não os listados, preceda-o com uma barra invertida (\) ou circunscreva-o entre aspas (" ").  <br/> |
|\ (caractere de barra invertida)  <br/> |Exibe o caractere seguinte na cadeia de caracteres de formato. Para exibir um caractere que tenha um significado especial como um caractere literal, preceda-o com uma barra invertida (\). A barra invertida não será exibida. Usar uma barra invertida é o mesmo que incluir o caractere seguinte entre aspas. Para exibir uma barra invertida, use duas barras invertidas (\\).  <br/> Exemplos de caracteres que não podem ser exibidos como caracteres literais são os caracteres de formatação de data e de formatação de hora (a, c, d, h, m, n, p, q, s, t, w, y, /, e :), os caracteres de formatação numérica (#, 0, %, E, e, vírgula e ponto) e os caracteres de formatação de cadeia de caracteres (@, &amp;, \<, \>, e !).  <br/> |
|"ABC"  <br/> |Exibe a cadeia de caracteres entre aspas (" "). Para incluir uma cadeia de caracteres no argumento de estilo dentro do código, você deve usar Chr(34) para circunscrever o texto (34 é o código de caractere para uma aspa (")).  <br/> |
   
A tabela a seguir contém algumas amostras de expressões de formato para números. (Todos os exemplos assumirão que a configuração de local do seu sistema é Inglês-EUA.) A primeira coluna contém as cadeias de caracteres de formato para a função Format. As outras colunas contêm a saída resultante se os dados formatados tiverem o valor dado nos títulos de coluna.
  
|**Format (Style)**|**"5" formatado como**|**"-5" formatado como**|**"0.5" formatado como**|**"0" formatado como**|
|:-----|:-----|:-----|:-----|:-----|
|Cadeia de caracteres de comprimento zero ("")  <br/> |5  <br/> |-5  <br/> |0.5  <br/> |0  <br/> |
|0  <br/> |5  <br/> |-5  <br/> |1  <br/> |0  <br/> |
|0.00  <br/> |5.00  <br/> |-5.00  <br/> |0.50  <br/> |0.00  <br/> |
|#,##0  <br/> |5  <br/> |-5  <br/> |1  <br/> |0  <br/> |
|$#,##0;($#,##0)  <br/> |$5  <br/> |($5)  <br/> |$1  <br/> |$0  <br/> |
|$#,##0.00;($#,##0.00)  <br/> |$5.00  <br/> |($5.00)  <br/> |$0.50  <br/> |$0.00  <br/> |
|0%  <br/> |500%  <br/> |-500%  <br/> |50%  <br/> |0%  <br/> |
|0.00%  <br/> |500.00%  <br/> |-500.00%  <br/> |50.00%  <br/> |0.00%  <br/> |
|0.00E+00  <br/> |5.00E+00  <br/> |-5.00E+00  <br/> |5.00E-01  <br/> |0.00E+00  <br/> |
|0.00E-00  <br/> |5.00E00  <br/> |-5.00E00  <br/> |5.00E-01  <br/> |0.00E00  <br/> |
|"$#,##0;;\Z\e\r\o"  <br/> |$5  <br/> |$-5  <br/> |$1  <br/> |Zero  <br/> |
   
## <a name="remarks"></a>Comentários
<a name="bk_addresources"> </a>

Se você incluir pontos e vírgulas com nada entre eles, a seção em falta será exibida usando o formato do valor positivo.
  
## <a name="see-also"></a>Confira também

- [Função Format (aplicativo Web personalizado do Access)](format-function-access-custom-web-app.md) 
- [Formatos de data e hora personalizados da função Format (aplicativo Web personalizado do Access)](custom-date-and-time-formats-for-the-format-function-access-custom-web-app.md)
  

