---
title: Formatos de data e hora personalizados da função Format (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f7d15fe6-bdad-4f1f-aa18-12a21fc111c4
description: Saiba como controlar como uma data ou hora é exibida criando uma formatação personalizada.
ms.openlocfilehash: 17724cfe1c26a2b3e52eea18dfef53aff027085c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765087"
---
# <a name="custom-date-and-time-formats-for-the-format-function-access-custom-web-app"></a>Formatos de data e hora personalizados da função Format (aplicativo Web personalizado do Access)

Saiba como controlar como uma data ou hora é exibida criando uma formatação personalizada.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="format-specifications"></a>Especificações de formato

A tabela a seguir lista caracteres que você pode usar com a função [Função Format (aplicativo da web personalizado do Access)](format-function-access-custom-web-app.md) para criar formatos de data e hora personalizados. 
  
|**Especificação de formato**|**Descrição**|
|:-----|:-----|
|(:)  <br/> |Separador de hora. Em alguns locais, outros caracteres podem ser usados para representar o separador de hora. O separador de hora separa as horas, os minutos e os segundos ao formatar valores de tempo. O caractere real usado como separador de tempo na saída formatada é determinado pelo valor de cultura atual do seu aplicativo.  <br/> |
|(/)  <br/> |Separador de data. Em alguns locais, outros caracteres podem ser usados para representar o separador de data. O separador de data separa o dia, mês e ano ao formatar valores de data. O caractere real usado como separador de data na saída formatada é determinado pela cultura atual do seu aplicativo.  <br/> |
|(%)  <br/> |Usado para indicar que o caractere seguinte deve ser lido como um formato de letra única sem considerar as letras à direita. Também é usado para indicar que o formato de letra única é lido como um formato definido pelo usuário. Consulte os itens seguintes para detalhes adicionais.  <br/> |
|d  <br/> |Exibe o dia como um número sem um zero à esquerda (por exemplo, 1). Use %d se este for o único caractere no seu formato numérico definido pelo usuário.  <br/> |
|dd  <br/> |Exibe o dia como um número com um zero à esquerda (por exemplo, 01).  <br/> |
|ddd  <br/> |Exibe o dia como uma abreviação (por exemplo, Dom).  <br/> |
|dddd  <br/> |Exibe o dia como um nome completo (por exemplo, Domingo).  <br/> |
|M  <br/> |Exibe o mês como um número sem um zero à esquerda (por exemplo, janeiro é representado como 1). Use %M se este for o único caractere no seu formato numérico definido pelo usuário.  <br/> |
|MM  <br/> |Exibe o mês como um número com um zero à esquerda (por exemplo, 01/12/01).  <br/> |
|MMM  <br/> |Exibe o mês como uma abreviação (por exemplo, Jan).  <br/> |
|MMMM  <br/> |Exibe o mês como um nome de mês completo (por exemplo, Janeiro).  <br/> |
|gg  <br/> |Exibe a cadeia de caracteres de período/era (por exemplo, A.D.).  <br/> |
|h  <br/> |Exibe a hora como um número sem zeros à esquerda usando o relógio de 12 horas (por exemplo, 1:15:15 PM). Use %h se este for o único caractere no seu formato numérico definido pelo usuário.  <br/> |
|hh  <br/> |Exibe a hora como um número com zeros à esquerda usando o relógio de 12 horas (por exemplo, 01:15:15 PM).  <br/> |
|H  <br/> |Exibe a hora como um número sem zeros à esquerda usando o relógio de 24 horas (por exemplo, 1:15:15). Use %H se este for o único caractere no seu formato numérico definido pelo usuário.  <br/> |
|HH  <br/> |Exibe a hora como um número sem zeros à esquerda usando o formato de 24 horas (por exemplo, 01:15:15).  <br/> |
|m  <br/> |Exibe o minuto como um número sem zeros à esquerda (por exemplo, 12:1:15). Use %m se este for o único caractere no seu formato numérico definido pelo usuário.  <br/> |
|mm  <br/> |Exibe o minuto como um número com zeros à esquerda (por exemplo, 12:01:15).  <br/> |
|s  <br/> |Exibe o segundo como um número sem zeros à esquerda (por exemplo, 12:15:5). Use %s se este for o único caractere no seu formato numérico definido pelo usuário.  <br/> |
|ss  <br/> |Exibe o segundo como um número com zeros à esquerda (por exemplo, 12:15:05).  <br/> |
|f  <br/> |Exibe frações de segundos. Por exemplo, ff exibe centésimos de segundos, enquanto fff exibe décimos de milésimos de segundos. Você pode usar até sete símbolos f no seu formato definido pelo usuário. Use %f se este for o único caractere no seu formato numérico definido pelo usuário.  <br/> |
|t  <br/> |Usa o relógio de 12 horas e exibe um A maiúsculo para qualquer hora antes do meio-dia; exibe um P maiúsculo para qualquer hora entre o meio-dia e 11:59 P.M. Use %t se este for o único caractere no seu formato numérico definido pelo usuário.  <br/> |
|tt  <br/> |Para locais que usem um relógio de 12 horas, exibe um AM em maiúsculas com qualquer hora antes do meio-dia; exibe um PM em maiúsculas com qualquer hora entre o meio-dia e 11:59 P.M.  <br/> Para locais que usem um relógio de 24 horas, não exibe nada.  <br/> |
|y  <br/> |Exibe o número de ano (0-9) sem zeros à esquerda. Use %y se este for o único caractere no seu formato numérico definido pelo usuário.  <br/> |
|yy  <br/> |Exibe o ano em formato numérico de dois dígitos com um zero à esquerda, se aplicável.  <br/> |
|yyy  <br/> |Exibe o ano em um formato numérico de quatro dígitos.  <br/> |
|yyyy  <br/> |Exibe o ano em um formato numérico de quatro dígitos.  <br/> |
||Exibe o deslocamento de fuso horário sem um zero à esquerda (por exemplo, -8). Use %z se este for o único caractere no seu formato numérico definido pelo usuário.  <br/> |
|z  <br/> |Exibe o deslocamento de fuso horário com um zero à esquerda (por exemplo, -08).  <br/> |
|zz  <br/> |Exibe o deslocamento de fuso horário com um zero à esquerda (por exemplo, -08)  <br/> |
|zzz  <br/> |Exibe o deslocamento de fuso horário completo (por exemplo, -08:00)  <br/> |
   
## <a name="remarks"></a>Observações

As cadeias de caracteres de formatação diferenciam maiúsculas de minúsculas. Formatações diferentes podem ser obtidas usando um caso diferente. Por exemplo, ao formatar um valor de data com a cadeia de caracteres "D", você obterá a data no formato longo (de acordo com o seu local atual). No entanto, se alterar o caso para "d", você obterá a data no formato curto. Além disso, resultados inesperados ou um erro podem ocorrer se a formatação pretendida não corresponder ao caso de nenhuma cadeia de caracteres de formato.
  
## <a name="see-also"></a>Confira também

- [Função Format (aplicativo da web personalizado do Access)](format-function-access-custom-web-app.md) 
- [Formatos numéricos personalizados da função Format (aplicativo Web personalizado do Access)](custom-numeric-formats-for-the-format-function-access-custom-web-app.md)
  

