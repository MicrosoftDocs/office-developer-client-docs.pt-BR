---
title: Método Open (Connection do ADO)
TOCTitle: Open Method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3bd698f7ea6c05d81e07969ae8031049804b7706
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889465"
---
# <a name="open-method-ado-connection"></a>Método Open (Connection do ADO)


**Aplica-se a**: Access 2013, o Office 2013
 

Abre uma conexão a uma fonte de dados.

## <a name="syntax"></a>Sintaxe

*conexão*. Abrir*ConnectionString*, *UserID*, *senha*, *Opções*

## <a name="parameters"></a>Parâmetros

  - *ConnectionString*

  - Opcional. Um valor **String** que contém informações de conexão. Consulte a propriedade [ConnectionString](connectionstring-property-ado.md) para obter detalhes sobre definições válidas.

  - *UserID*

  - Opcional. Um valor **String** que contém um nome de usuário que será utilizado ao estabelecer a conexão.

  - *Password*

  - Opcional. Um valor **String** que contém uma senha que será utilizada ao estabelecer a conexão.

  - *Options*

  - Opcional. Um valor [ConnectOptionEnum](connectoptionenum.md) que determina se esse método deve retornar depois (sincronamente) ou antes (assincronamente) de a conexão ser estabelecida.

## <a name="remarks"></a>Comentários

A utilização do método **Open** em um objeto [Connection](connection-object-ado.md) estabelece a conexão física a uma fonte de dados. Depois da conclusão com êxito desse método, a conexão estará ativa e será possível emitir comandos com relação à mesma e processar os resultados.

Use o argumento *ConnectionString* opcional para especifique uma cadeia de caracteres de conexão que contém uma série de instruções de *= o valor* do *argumento* separadas por ponto e vírgula ou um arquivo ou identificado com uma URL de recurso de diretório. A propriedade **ConnectionString** herda automaticamente o valor usado para o argumento *ConnectionString* . Portanto, você pode definir a propriedade **ConnectionString** do objeto de **Conexão** antes de abri-lo, ou usar o argumento *ConnectionString* para definir ou substituir os parâmetros de conexão atual durante a chamada do método **Open** .

Se você passar informações de usuário e senha no argumento *ConnectionString* e nos argumentos opcionais *UserID* e *Password*, os argumentos *UserID* e *Password* substituirão os valores especificados em *ConnectionString*.

Quando concluir as operações em um **Connection** aberto, utilize o método [Close](close-method-ado.md) para liberar quaisquer recursos associados do sistema. O fechamento de um objeto não o remove da memória; é possível alterar as definições de propriedade e utilizar o método **Open** para abri-lo novamente mais tarde. Para eliminar completamente um objeto da memória, defina a variável do objeto como *Nothing*.

**Uso de serviço de dados remotos** Quando usado em um objeto de **Conexão** do cliente, o método **Open** realmente não estabelece uma conexão ao servidor, até que um [conjunto de registros](recordset-object-ado.md) é aberto no objeto de **Conexão** .


> [!NOTE]
> [!OBSERVAçãO] URLs que utilizem o esquema http chamarão automaticamente o [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).


