---
title: Propriedade CommandText (ADO)
TOCTitle: CommandText property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 86f69be8ed9216619f10bc70e2c701fb109d0ff5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879302"
---
# <a name="commandtext-property-ado"></a>Propriedade CommandText (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o texto de um comando a ser emitido para um provedor.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String** contendo um comando de provedor, como uma instrução SQL, um nome de tabela, uma URL relativa ou uma chamada de procedimento armazenado. O padrão é "" (sequência de comprimento zero).

## <a name="remarks"></a>Comentários

Use a propriedade **CommandText** para definir ou retornar o texto de um comando representado por um objeto [Command](command-object-ado.md). Geralmente, é uma instrução SQL, mas também pode ser qualquer outro tipo de instrução de comando reconhecida pelo provedor, como uma chamada de procedimento armazenado. Uma instrução SQL deve ser de um dialeto ou versão específica que tenha suporte do processador de consultas do provedor.

Se a propriedade [Prepared](prepared-property-ado.md) do objeto **Command** estiver definida como **True** e o objeto **Command** estiver vinculado a uma conexão aberta quando você definir a propriedade **CommandText**, o ADO preparará a consulta (isto é, um formulário compilado da consulta que é armazenado pelo provedor) quando você chamar os métodos [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) ou **Open**.

Dependendo da definição da propriedade [CommandType](commandtype-property-ado.md), o ADO poderá alterar a propriedade **CommandText**. Você pode ler a propriedade **CommandText** a qualquer momento para ver o texto de comando real que será utilizado pelo ADO durante a execução.

Use a propriedade **CommandText** para definir ou retornar uma URL relativa que especifique um recurso, como um arquivo ou um diretório. O recurso é relativo a um local especificado explicitamente por uma URL absoluta ou implicitamente por um objeto [Connection](connection-object-ado.md) aberto.


> [!NOTE]
> [!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).


