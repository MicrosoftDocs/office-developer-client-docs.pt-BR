---
title: Sobre Figuras de Formatação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251831
localization_priority: Normal
ms.assetid: df4c1c70-8b41-c046-7415-643188af0e06
description: Uma figura de formatação é utilizada para determinar como um valor é exibido. Por exemplo, é possível controlar o número de dígitos exibidos à direita ou à esquerda de um ponto decimal ou se uma cadeia de caracteres será exibida em letras maiúsculas ou minúsculas.
ms.openlocfilehash: 7043c9819f41ec2c08345c84010328be75677918
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436815"
---
# <a name="about-format-pictures"></a>Sobre Figuras de Formatação

Uma figura de formatação é utilizada para determinar como um valor é exibido. Por exemplo, é possível controlar o número de dígitos exibidos à direita ou à esquerda de um ponto decimal ou se uma cadeia de caracteres será exibida em letras maiúsculas ou minúsculas.
  
> [!NOTE]
> Para definir uma imagem de formatação de data ou hora usando a formatação do Microsoft Office system, coloque a imagem de formatação entre chaves duplas; por exemplo, "{{m/d/aa}}". Se você estiver usando um formato predefinido, por exemplo, 201, coloque-o entre chaves e colchetes angulares, da seguinte forma:\<"\>{201}" 
  
As seções a seguir mostram símbolos que você pode usar para formatar diferentes tipos de valores para exibição.
  
## <a name="string-and-numeric-values"></a>Valores numéricos e de sequência de caracteres

|**Caractere**|**Descrição**|
|:-----|:-----|
|#  <br/> |Espaço reservado para dígito. Exibe um dígito ou nada. Zeros à esquerda e à direita não são exibidos. Se mais dígitos do que espaços reservados para dígito estiverem à esquerda do decimal, todos os dígitos serão exibidos. Se mais dígitos do que espaços reservados para dígito estiverem à direita do decimal, a fração será arredondada para o número de espaços. Para uma dimensão, se o espaço for o último dígito à esquerda, as subunidades 0 não são exibidas.  <br/> Por exemplo, FORMAT(0pé 11.25pol,"#.##u") exibe 11,25pol.  <br/> |
|,0  <br/> |Espaço reservado para dígito (zero). Exibe um dígito ou nada. Zeros à esquerda e à direita são exibidos. Se mais dígitos do que espaços reservados para dígito estiverem à esquerda do decimal, todos os dígitos serão exibidos. Se mais dígitos do que espaços reservados para dígito estiverem à direita do decimal, a fração será arredondada para o número de espaços. Para uma dimensão, as subunidades 0 são exibidas.  <br/> Por exemplo, FORMAT(2pés 11.33pol,"0.## u") exibe 2 pés 11,33 pol.  <br/> |
|.  <br/> |Espaço reservado para decimal. Determina quantos dígitos serão exibidos à esquerda e à direita da posição decimal. Em uma unidade de diversas partes, o decimal é utilizado na menor subunidade (da extrema direita). Exibe o caractere decimal definido nas configurações **Região e Idioma** do sistema (Painel de Controle).<br/> Por exemplo, FORMAT(250 cm,"0.000 u") exibe 250,000 cm.  <br/> |
|,  <br/> |Separador de milhar. Se acompanhado de espaços reservados para dígito (# ou 0) será utilizado para separar milhares de centenas em um número que contenha quatro ou mais dígitos à esquerda do decimal. Exibe o separador de milhar definido nas configurações **Região e Idioma** do sistema (Painel de Controle).<br/> |
|E- E+ e- e+  <br/> |Formato científico. Se o formato contiver pelo menos um espaço reservado para dígito à direita desses símbolos, o número será exibido em formato científico. Insere o E ou e entre o número e seu exponente. Para E+ ou e+, exibe o sinal de mais (+) antes de exponentes positivos e o sinal de menos (-) antes de exponentes negativos. Para E- ou e-, exibe o sinal de menos (-) somente quando o exponente é negativo.  <br/> Por exemplo, FORMAT(12345.67,"###.#e+#") exibe 123.5e+2.  <br/> |
|u ou U  <br/> |Espaço reservado para rótulo curto. Insere rótulos de unidade abreviados depois de cada subunidade. Por exemplo: pol., pé, grau. O espaço reservado U insere rótulos de casos mistos, enquanto o espaço reservado u insere rótulos em minúsculas. Insere o mesmo número de espaços antes do rótulo e do espaço reservado.  <br/> Por exemplo, FORMAT(12 c 13 d,"#u") exibe 13c1.  <br/> |
|uu ou UU  <br/> |Espaço reservado para rótulo longo. Insere rótulos de unidade depois de cada subunidade. Por exemplo: polegadas, pés, graus o espaço reservado U insere rótulos de maiúsculas e minúsculas, enquanto o espaço reservado U insere rótulos em minúsculas. Insere o mesmo número de espaços antes do rótulo e do espaço reservado.  <br/> Por exemplo, FORMAT(12.43pol,"# #/4 UU") exibe 12 2/4 POLEGADAS.  <br/> |
|uuu ou UUU  <br/> |Espaço reservado para rótulo universal. Insere o formulário universal de rótulos de unidade (interno para o Visio) após cada subunidade. O espaço reservado U insere rótulos de casos mistos, enquanto o espaço reservado u insere rótulos em minúsculas. Insere o mesmo número de espaços antes do rótulo e do espaço reservado.  <br/> |
|/  <br/> |Espaço reservado para fração. Exibe a expressão como um número inteiro com fração se um espaço reservado para dígito à esquerda estiver presente. Caso contrário, exibe somente o número inteiro no numerador. Se um número seguir o espaço reservado para dígito no denominador, a fração será arredondada para a fração mais próxima, cujo numerador seja 1, e simplificada. Se um número for especificado no denominador sem o espaço reservado para dígito, a fração será arredondada, mas não simplificada.  <br/> Por exemplo, FORMAT(12.43,"# #/4") exibe 12 2/4.  <br/> |
|espaço  <br/> |Exibe um caractere de espaço na saída formatada. Para exibir outro caractere, use a barra invertida\) (caractere.  <br/> |
   
## <a name="currency-values"></a>Valores de moeda.

|**Caractere**|**Descrição**|
|:-----|:-----|
|$  <br/> |Símbolo de moeda. Exibe o símbolo de moeda definido para as configurações **Região e Idioma** do sistema (Painel de Controle).  <br/> |
|u ou U  <br/> |Espaço reservado para rótulo curto. Insere o símbolo padrão para a moeda local ou as abreviaturas de moeda de três caracteres para moedas que não sejam locais. Por exemplo, $99.00, 42.70 FRF. O espaço reservado u insere em minúsculas e U insere rótulos de maiúsculas e minúsculas.  <br/> |
|uu ou UU  <br/> |Espaço reservado para rótulo longo. Insere rótulos de moeda longos depois de cada subunidade. Por exemplo: dólar americano, francos franceses. O espaço reservado u insere em minúsculas e U insere rótulos de maiúsculas e minúsculas.  <br/> |
|uuu ou UUU  <br/> |Espaço reservado para rótulo universal. Insere as abreviaturas universais de moeda de três caracteres para todas as moedas depois de cada subunidade. Por exemplo, 99.00 USD, 42.70 FRF. O espaço reservado u insere em minúsculas e U insere rótulos de maiúsculas e minúsculas. Insere o mesmo número de espaços antes do rótulo e do espaço reservado.  <br/> |
   
## <a name="text-values"></a>Valores de texto

|**Caractere**|**Descrição**|
|:-----|:-----|
|\  <br/> |Exibe o caractere seguinte como está. Para exibir o caractere de barra invertida \\, digite. Consulte também "text".  <br/> |
|"text" ou 'text'  <br/> |Exibe o texto entre aspas como está. Consulte também \ (barra invertida).  <br/> |
|@  <br/> |Espaço reservado para texto. Substitui uma sequência de caracteres se o valor de uma expressão for uma sequência de caracteres.  <br/> Por exemplo, FORMAT("Olá", "'Você digitou ('@')'" ) resulta em "Você digitou (Olá)".  <br/> |
|@+  <br/> |Espaço reservado para texto de letras maiúsculas. Para valores de sequência de caracteres, substitui a entrada por letras maiúsculas.  <br/> Por exemplo, FORMAT("Olá", "@ @+ @-" ) resulta me "Olá OLÁ olá)".  <br/> |
|@-  <br/> |Espaço reservado para texto. Para valores de sequência de caracteres, substitui a entrada por letras minúsculas.  <br/> Por exemplo, FORMAT("Olá", "@ @+ @-" ) resulta em "Olá OLÁ olá)".  <br/> |
   
## <a name="date-values"></a>Valores de data

|**Caractere**|**Descrição**|
|:-----|:-----|
|c ou C  <br/> |Espaço reservado para hora ou data. Exibe os valores de data e hora usando formatos de data curto (c) ou longo (C) e o formato de hora geral. As versões 4.0 e posteriores do Visio ignoram esse espaço reservado.  <br/> Por exemplo: FORMAT(DATETIME("6/25/07 12:05"),"C") exibe Segunda-feira, 25 de junho de 2007 12:05:00 PM. FORMAT(DATETIME("25 de junho de 2007"),"c") exibe 25/6/2007.  <br/> |
|/  <br/> |Separador de data. Se a expressão for uma data, separa os componentes da data. Exibe o separador de data definido para as configurações **Região e Idioma** do sistema (Painel de Controle).<br/> |
| [ ]  <br/> |Espaço reservado para data decorrida. Utilizado com os espaços reservados d, dd, s e ss para exibir as unidades de duração.  <br/> Por exemplo, [d] ou [dd] indica dias decorridos e [s] ou [ss], semanas decorridas.  <br/> |
|d  <br/> |Espaço reservado para dia. Exibe o dia como um número (1-31) sem um zero à esquerda.  <br/> |
|dd  <br/> | Espaço reservado para dia. Exibe o dia como um número (01-31) com um zero à esquerda.  <br/> |
|ddd ou s  <br/> |Espaço reservado para dia da semana curto. Exibe o dia como uma abreviatura (Dom-Sáb).  <br/> |
|dddd ou w  <br/> |Espaço reservado para dia da semana longo. Exibe o dia como um nome completo (Domingo-Sábado).  <br/> |
|ddddd  <br/> |Espaço reservado para data curta. Exibe uma data no formato curto definido para as configurações **Região e Idioma** do sistema (Painel de Controle).<br/> |
|dddd  <br/> |Espaço reservado para data longa. Exibe uma data no formato longo definido para as configurações **Região e Idioma** do sistema (Painel de Controle).  <br/> |
|D  <br/> |Espaço reservado para dia do chinês tradicional. Exibe o dia do mês como uma representação textual do número ordinal. Específico ao local.  <br/> |
|D_c  <br/> |Espaço reservado para dia do chinês tradicional. Exibe o dia do mês como uma representação textual do número ordinal. Independente do local do usuário.  <br/> |
|w_c ou w_c  <br/> |Espaço reservado para dia do chinês tradicional. Independente do local do usuário.  <br/> |
|w_e  <br/> |Espaço reservado para dia da semana curto do português. Exibe o dia como uma abreviatura (Dom-Sáb). Independente do local do usuário.  <br/> |
|w_j  <br/> |Espaço reservado para dia da semana curto do japonês. Exibe o dia como uma abreviatura. Independente do local do usuário.  <br/> |
|w_k  <br/> |Espaço reservado para dia da semana curto do coreano. Exibe o dia como uma abreviatura. Independente do local do usuário.  <br/> |
|w_s ou w_s  <br/> |Espaço reservado para dia do chinês simplificado. Independente do local do usuário.  <br/> |
|ww_e  <br/> |Espaço reservado para dia da semana longo do português. Exibe o dia como um nome completo (Domingo-Sábado). Independente do local do usuário.  <br/> |
|ww_j  <br/> |Espaço reservado para dia da semana longo do japonês. Exibe o dia como um nome completo. Independente do local do usuário.  <br/> |
|w_k  <br/> |Espaço reservado para dia da semana longo do coreano. Exibe o dia como um nome completo. Independente do local do usuário.  <br/> |
|M  <br/> |Espaço reservado para mês. Exibe o mês como um número (1-12) sem um zero à esquerda. Consulte também m (espaço reservado para minuto).  <br/> |
|MM  <br/> |Espaço reservado para mês. Exibe o mês como um número (01-12) com um zero à esquerda. Consulte também mm (espaço reservado para minuto).  <br/> |
|MMM  <br/> |Espaço reservado para mês. Exibe o mês na forma abreviada (Jan-Dez).  <br/> |
|MMMM  <br/> |Espaço reservado para mês. Exibe o nome inteiro do mês (Janeiro-Dezembro).  <br/> |
|MMMM_c  <br/> |Espaço reservado para mês do chinês tradicional. Exibe o nome completo do mês. Independente do local do usuário.  <br/> |
|MMMM_e  <br/> |Espaço reservado para mês do inglês. Exibe o nome completo do mês. Independente do local do usuário.  <br/> |
|yy  <br/> |Espaço reservado para ano. Exibe o ano como um número de dois dígitos (00-99).  <br/> |
|aaaa  <br/> |Espaço reservado para ano. Exibe o ano como um número de quatro dígitos (1900-2078).  <br/> |
|g  <br/> |Espaço reservado para ano. Específico ao local. Para japonês, exibe a versão curta da Era Gengo. Para coreano, exibe o rótulo de ano coreano seguido de um espaço.  <br/> |
|g_j  <br/> |Espaço reservado para ano. Para japonês, exibe a versão curta da Era Gengo. Independente do local do usuário.  <br/> |
|gg ou G  <br/> |Espaço reservado para ano. Específico ao local. Para chinês tradicional, exibe uma versão curta para o rótulo anual formal. Para japonês, exibe a versão curta da Era Gengo em Kanji. Para coreano, exibe o rótulo de ano coreano seguido de um espaço.  <br/> |
|gg_c  <br/> |Espaço reservado para ano. Para chinês tradicional, exibe a versão curta para o rótulo do ano formal. Independente do local do usuário.  <br/> |
|gg_j  <br/> |Espaço reservado para ano. Para japonês, exibe a versão curta da Era Gengo em Kanji. Independente do local do usuário.  <br/> |
|gg_k  <br/> |Espaço reservado para ano. Para coreano, exibe o rótulo de ano coreano seguido de um espaço. Independente do local do usuário.  <br/> |
|ggg ou GG  <br/> |Espaço reservado para ano. Específico ao local. Para chinês tradicional, exibe uma versão longa para o rótulo anual formal. Para japonês, exibe a versão longa da Era Gengo em Kanji. Para coreano, exibe o rótulo de ano coreano seguido de um espaço.  <br/> |
|ggg_c  <br/> |Espaço reservado para ano. Para chinês tradicional, exibe a versão longa para o rótulo do ano formal. Independente do local do usuário.  <br/> |
|ggg_j  <br/> |Espaço reservado para ano. Para japonês, exibe a versão longa da Era Gengo em Kanji. Independente do local do usuário.  <br/> |
|minúscula  <br/> |Espaço reservado para ano. Específico ao local. Para chinês tradicional, exibe uma sequência de caracteres que representa o ano juliano. Para japonês, exibe o ano Gengo como um ou dois dígitos e nenhum zero à esquerda. Para coreano, exibe o ano coreano como numeral arábico de quatro dígitos.  <br/> |
|e_c  <br/> |Espaço reservado para ano. Para chinês tradicional, exibe uma sequência de caracteres que representa o ano juliano. Independente do local do usuário.  <br/> |
|E_J  <br/> |Espaço reservado para ano. Para japonês, exibe o ano Gengo como um numeral arábico de um ou dois dígitos. Independente do local do usuário.  <br/> |
|e_k  <br/> |Espaço reservado para ano. Para coreano, exibe o ano coreano como numeral arábico de quatro dígitos. Independente do local do usuário.  <br/> |
|E  <br/> |Espaço reservado para ano. Específico ao local. Para chinês tradicional, exibe uma sequência de caracteres que representa o ano republicano. Para japonês, exibe o ano Gengo como um ou dois dígitos e nenhum zero à esquerda. Para coreano, exibe o ano coreano como um numeral arábico de quatro dígitos.  <br/> |
|E_c  <br/> |Espaço reservado para ano. Para chinês tradicional, exibe uma sequência de caracteres que representa o ano republicano. Independente do local do usuário.  <br/> |
|aplicação  <br/> |Espaço reservado para ano. Específico ao local. Para chinês tradicional, exibe uma sequência de caracteres que representa o ano juliano. Para japonês, exibe o ano Gengo como um numeral arábico de dois dígitos com zero à esquerda, se necessário. Para coreano, exibe o ano coreano como um numeral arábico de quatro dígitos.  <br/> |
|ee_j  <br/> |Espaço reservado para ano. Para japonês, exibe o ano Gengo como um numeral arábico de dois dígitos. Independente do local do usuário.  <br/> |
|APLICAÇÃO  <br/> |Espaço reservado para ano. Específico ao local. Para chinês tradicional, exibe uma sequência de caracteres que representa o ano republicano. Para japonês, exibe o ano Gengo como um numeral arábico de dois dígitos com zero à esquerda, se necessário. Para coreano, exibe o ano coreano como um numeral arábico de quatro dígitos.  <br/> |
|n ou N  <br/> |Espaço reservado para ano. Específico ao local. Para chinês tradicional, exibe o ano republicano como um numeral arábico. Para japonês, exibe o ano Gengo como um numeral arábico de um ou dois dígitos e nenhum zero à esquerda. Para coreano, exibe o ano coreano como um numeral arábico de quatro dígitos.  <br/> |
|n_c  <br/> |Espaço reservado para ano. Para chinês tradicional, exibe o ano republicano como um numeral arábico. Independente do local do usuário.  <br/> |
|nn ou NN  <br/> |Espaço reservado para ano. Específico ao local. Para chinês tradicional, exibe o ano republicano como um numeral arábico. Para japonês, exibe o ano Gengo como um numeral arábico de dois dígitos com zero à esquerda, se necessário. Para coreano, exibe o ano coreano como um numeral arábico de quatro dígitos.  <br/> |
   
## <a name="time-values"></a>Valores de hora

|**Caractere**|**Descrição**|
|:-----|:-----|
|:  <br/> |Separador de hora. Exibe a hora definida para as configurações **Região e Idioma** do sistema (Painel de Controle).<br/> |
|[ ]  <br/> |Espaço reservado para tempo decorrido. Usado com espaços reservados de h, hh, m, mm, s e ss para exibir unidades de duração. Por exemplo, [h] ou [hh] significa horas decorridas, [m] ou [mm] significa minutos decorridos e [s] ou [ss] significa segundos decorridos.  <br/> |
|h  <br/> |Espaço reservado para hora. Exibe a hora sem um zero à esquerda no formato de 12 horas (0-12).  <br/> |
|hh  <br/> |Espaço reservado para hora. Exibe a hora com um zero à esquerda no formato de 12 horas (00-12).  <br/> |
|H  <br/> |Espaço reservado para hora. Exibe a hora sem um zero à esquerda no formato de 24 horas (0-24).  <br/> |
|HH  <br/> |Espaço reservado para hora. Exibe a hora com um zero à esquerda no formato de 24 horas (00-24).  <br/> |
|m  <br/> |Espaço reservado para minuto. Exibe os minutos sem um zero à esquerda (0-59).  <br/> |
|mm  <br/> |Espaço reservado para minuto. Exibe os minutos com um zero à esquerda (00-59).  <br/> |
|s  <br/> |Espaço reservado para segundo. Exibe os segundos sem um zero à esquerda (0-59).  <br/> |
|ss  <br/> |Espaço reservado para segundo. Exibe os segundos com um zero à esquerda (00-59).  <br/> |
|t  <br/> |Abreviação AM/PM. Exibe a abreviação definida para as configurações **Região e Idioma** do sistema (Painel de Controle).<br/> |
|tt  <br/> |Designador AM/PM. Exibe o designador definido para as configurações **Região e Idioma** do sistema (Painel de Controle).<br/> |
|t_c ou tt_c  <br/> |Designador AM/PM do chinês tradicional. Exibe o designador. Independente do local do usuário.  <br/> |
|t_k ou tt_k  <br/> |Designador AM/PM do coreano. Exibe o designador. Independente do local do usuário.  <br/> |
|t_j ou tt_j  <br/> |Designador AM/PM do japonês. Exibe o designador. Independente do local do usuário.  <br/> |
|t_e  <br/> |Designador AM/PM do inglês. Exibe o designador curto. Independente do local do usuário.  <br/> |
|tt_e  <br/> |Designador AM/PM do inglês. Exibe o designador completo. Independente do local do usuário.  <br/> |
|t_s ou tt_s  <br/> |Designador AM/PM do chinês simplificado. Exibe o designador. Independente do local do usuário.  <br/> |
|T  <br/> |Formato de tempo geral.  <br/> |
   

