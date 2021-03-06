---
title: Objeto Command (ADO)
TOCTitle: Command object (ADO)
ms:assetid: 64f4ef03-f858-c004-b891-0c96d13a5e6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249389(v=office.15)
ms:contentKeyID: 48545303
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231106
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dc582046ff1981a82fab9c9c551b0064c1e8c1de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296168"
---
# <a name="command-object-ado"></a>Objeto Command (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Define um comando específico que você pretende executar em relação a uma fonte de dados.

## <a name="remarks"></a>Comentários

Use um objeto **Command** para consultar um banco de dados e retornar registros em um objeto [Recordset](recordset-object-ado.md), para executar uma operação em massa ou manipular a estrutura de um banco de dados. Dependendo da funcionalidade do provedor, alguns métodos e algumas coleções e propriedades **Command** poderão gerar um erro quando mencionados.

Com as coleções, os métodos e as propriedades de um objeto **Command**, você pode fazer o que segue:

  - Definir o texto executável do comando (por exemplo, uma instrução SQL) com a propriedade [CommandText](commandtext-property-ado.md).

  - Definir consultas com parâmetros ou argumentos de procedimentos armazenados usando objetos [Parameter](parameter-object-ado.md) e a coleção [Parameters](parameters-collection-ado.md).

  - Executar um comando e retornar um objeto **Recordset**, se for adequado, com o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).

  - Especificar o tipo de comando com a propriedade [CommandType](commandtype-property-ado.md) antes da execução para otimizar o desempenho.

  - Controlar se o provedor salvará uma versão preparada (ou compilada) do comando antes da execução com a propriedade [Prepared](prepared-property-ado.md).

  - Definir o número de segundos que um provedor aguardará um comando para executar a propriedade [CommandTimeout](commandtimeout-property-ado.md).

  - Associar uma conexão aberta com um objeto **Command** definindo sua propriedade [ActiveConnection](activeconnection-property-ado.md).

  - Definir a propriedade [Name](name-property-ado.md) para identificar o objeto **Command** como um método no objeto [Connection](connection-object-ado.md) associado.

  - Passar um objeto **Command** para a propriedade [Source](source-property-ado-recordset.md) de um **Recordset** para obter dados.

  - Acessar os atributos específicos do provedor com a coleção [Properties](properties-collection-ado.md).

> [!NOTE]
> [!OBSERVAçãO] Para executar uma consulta sem usar um objeto **Command**, passe uma sequência de consulta para o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) de um objeto **Connection** ou para o método [Open](open-method-ado-recordset.md) de um objeto **Recordset**. No entanto, um objeto **Command** será necessário quando você quiser insistircom o texto de comando e reexecutá-lo ou usar os parâmetros de consulta.

Para criar um objeto **Command**, de forma independente, de um objeto **Connection** definido anteriormente, defina a propriedade **ActiveConnection** como uma sequência de conexão válida. O ADO ainda criará um objeto **Connection**, mas não atribuirá esse objeto a uma variável de objeto. No entanto, se você estiver associando vários objetos **Command** com a mesma conexão, deverá criar e abrir, de forma explícita, um objeto **Connection**; isso atribui o objeto **Connection** a uma variável de objeto. Se você não definir a propriedade **ActiveConnection** do objeto **Command** para esta variável de objeto, o ADO criará um novo objeto **Connection** para cada objeto **Command**, mesmo se você usar a mesma sequência de conexão.

Para executar um objeto **Command**, basta chamá-lo por meio da propriedade [Name](name-property-ado.md) do objeto **Connection** associado. **Command** deve ter a propriedade **ActiveConnection** definida como o objeto **Connection**. Se **Command** tiver parâmetros, passe seus valores como argumentos para o método.

Se dois ou mais objetos **Command** forem executados na mesma conexão e o objeto **Command** estiver em um procedimento armazenado com parâmetros de saída, ocorrerá um erro. Para executar cada objeto **Command**, use conexões separadas ou desconecte todos os outros objetos **Command** da conexão.

A coleção **Parameters** é o membro padrão do objeto **Command**. Como resultado, as duas instruções de código a seguir são equivalentes.

