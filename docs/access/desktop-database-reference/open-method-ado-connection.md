---
title: Método Open (Connection do ADO)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b83eb87b181320c86e1aea91ede70cd173a5ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288424"
---
# <a name="open-method-ado-connection"></a>Método Open (Connection do ADO)

**Aplica-se ao:** Access 2013, Office 2013
 
Abre uma conexão a uma fonte de dados.

## <a name="syntax"></a>Sintaxe

*conexão*. *ConnectionString*aberta, *userid*, *senha*, *Opções*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*ConnectionString* |Opcional. Um valor **String** que contém informações de conexão. Consulte a propriedade [ConnectionString](connectionstring-property-ado.md) para obter detalhes sobre definições válidas.|
|*UserID* |Opcional. Um valor **String** que contém um nome de usuário que será utilizado ao estabelecer a conexão.|
|*Password* |Opcional. Um valor **String** que contém uma senha que será utilizada ao estabelecer a conexão.|
|*Options* |Opcional. Um valor [ConnectOptionEnum](connectoptionenum.md) que determina se esse método deve retornar depois (sincronamente) ou antes (assincronamente) de a conexão ser estabelecida.|

## <a name="remarks"></a>Comentários

A utilização do método **Open** em um objeto [Connection](connection-object-ado.md) estabelece a conexão física a uma fonte de dados. Depois da conclusão com êxito desse método, a conexão estará ativa e será possível emitir comandos com relação à mesma e processar os resultados.

Use o argumento *ConnectionString* opcional para especificar uma cadeia de caracteres de conexão contendo uma série de instruções *Argument* *= Value* separadas por ponto-e-vírgula ou um recurso de arquivo ou diretório identificado com uma URL. A propriedade **ConnectionString** herda automaticamente o valor utilizado para o argumento *ConnectionString*. Portanto, é possível definir a propriedade **ConnectionString** do objeto **Connection** antes de abri-lo ou utilizar o argumento *ConnectionString* para definir ou substituir os parâmetros da conexão atual durante a chamada ao método **Open**.

Se você passar informações de usuário e senha no argumento *ConnectionString* e nos argumentos opcionais *UserID* e *Password*, os argumentos *UserID* e *Password* substituirão os valores especificados em *ConnectionString*.

Quando concluir as operações em um **Connection** aberto, utilize o método [Close](close-method-ado.md) para liberar quaisquer recursos associados do sistema. O fechamento de um objeto não o remove da memória; é possível alterar as definições de propriedade e utilizar o método **Open** para abri-lo novamente mais tarde. Para eliminar completamente um objeto da memória, defina a variável do objeto como *Nothing*.

**Uso do Remote Data Service** Quando usado em um objeto **Connection** do lado do cliente, o método **Open** não estabelece realmente uma conexão com o servidor até que um [Recordset](recordset-object-ado.md) seja aberto no objeto **Connection** .

> [!NOTE]
> [!OBSERVAçãO] URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).


