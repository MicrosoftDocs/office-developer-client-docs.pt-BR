---
title: Programação ADO/WFC
TOCTitle: ADO/WFC Programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88343d14a9419cbc3425e0c21dee08d243f2e697
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462476"
---
# <a name="adowfc-programming"></a>Programação ADO/WFC


**Aplica-se a**: Access 2013 | Office 2013

Para o Microsoft Visual J++ 6.0, o ADO foi estendido para trabalhar com o WFC (Windows Foundation Classes) das seguintes maneiras. Primeiramente, um conjunto de classes Java foi implementado estendendo as interfaces ADO e criando notificações de interesse ao programador Java; as classes Java também expõem funções que retornam tipos Java ao usuário. Para aprimorar o desempenho, a classe Java acessa diretamente os tipos de dados nativos no objeto do conjunto de linhas OLE DB e os retorna ao programador Java como tipos Java sem convertê-los primeiro de e para uma variante. O ADO também foi estendido pra trabalhar com notificações de eventos na estrutura WFC.

O ADO para Windows Foundation Classes (ADO/WFC) suporta todos os métodos, propriedades, objetos e eventos do ADO padrão. No entanto, as operações que requerem uma variante como um parâmetro e mostram excelente desempenho em uma linguagem como Microsoft Visual Basic, exibem menos desempenho em uma linguagem como Visual J++. Por esse motivo, o ADO/WFC também fornece funções de acesso no objeto [Field](field-object-ado.md) que assume tipos de dados Java nativos em vez do tipo de dados da variante.

Para obter informações mais detalhadas dentro da documentação ADO sobre os pacotes ADO/WFC, consulte o [ADO/WFC Syntax Index](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).

## <a name="referencing-the-library"></a>Fazendo referência à biblioteca

Para importar as classes de dados ADO/WFC em seu projeto, inclua a seguinte linha em seu código:

```java 
 
import com.ms.wfc.data.*; 
```
