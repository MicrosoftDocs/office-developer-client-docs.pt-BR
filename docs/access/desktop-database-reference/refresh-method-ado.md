---
title: Método Refresh (ADO)
TOCTitle: Refresh method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c4bbc44dbb9cdfeaac0904ed5296db206016211d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922759"
---
# <a name="refresh-method-ado"></a>Método Refresh (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Atualiza os objetos de uma coleção para refletir os objetos disponíveis no provedor e específicos a ele.

## <a name="syntax"></a>Sintaxe

*coleção*. Atualizar

## <a name="remarks"></a>Comentários

O método **Refresh** executa diferentes tarefas, dependendo da coleção a partir do qual ele for chamado.

## <a name="parameters"></a>Parâmetros

O uso do método **Refresh** na coleção [Parameters](command-object-ado.md) de um objeto [Command](parameters-collection-ado.md) recupera informações de parâmetro do provedor para o procedimento armazenado ou a consulta com parâmetros especificada no objeto **Command**. A coleção estará vazia para os provedores que não oferecem suporte a chamadas de procedimento armazenado ou a consultas com parâmetros.

Defina a propriedade [ActiveConnection](activeconnection-property-ado.md) do objeto **Command** como um objeto [Connection](connection-object-ado.md) válido, a propriedade [CommandText](commandtext-property-ado.md) como um comando válido e a propriedade [CommandType](commandtype-property-ado.md) como **adCmdStoredProc** antes de chamar o método **Refresh**.

Se você acessar a coleção **Parameters** antes de chamar o método **Refresh**, o ADO chamará o método automaticamente e preencherá a coleção para você.


> [!NOTE]
> <P>[!OBSERVAçãO] Se você usar o método <STRONG>Refresh</STRONG> para obter informações de parâmetros a partir do provedor e ele retornar um ou mais objetos <A href="parameter-object-ado.md">Parameter</A> de tipo de dados de comprimento variável, o ADO poderá alocar memória para os parâmetros com base em seu tamanho potencial máximo, causando erro durante a execução. Defina explicitamente a propriedade <A href="size-property-ado.md">Size</A> para esses parâmetros antes de chamar o método <A href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute</A> a fim de evitar erros.</P>



**Campos**

O uso do método **Refresh** na coleção **Fields** não produz nenhum efeito visível. Para recuperar as alterações da estrutura de banco de dados subjacente, use o método [Requery](requery-method-ado.md) ou, se o objeto [Recordset](recordset-object-ado.md) não oferecer suporte a indicadores, o método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).

**Propriedades**

O uso do método **Refresh** em uma coleção **Properties** de alguns objetos preenche a coleção com as propriedades dinâmicas expostas pelo provedor. Essas propriedades fornecem informações sobre a a funcionalidade específica do provedor, além das propriedades internas compatíveis com o ADO.

