---
title: Modelo de programação do RDS em detalhes
TOCTitle: RDS programming model in detail
ms:assetid: 133fc059-9b51-52e2-2e61-339716d8d965
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248906(v=office.15)
ms:contentKeyID: 48543364
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a2312be682ee63368397109377690b6dde3e627
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300865"
---
# <a name="rds-programming-model-in-detail"></a>Modelo de programação do RDS em detalhes

**Aplica-se ao:** Access 2013, Office 2013

O modelo de programação RDS é formado por estes elementos-chave:

- RDS. DataSpace
- RDSServer.DataFactory
- RDS. DataControl
- Evento

## <a name="rdsdataspace"></a>RDS. DataSpace

Seu aplicativo cliente deve especificar o servidor e o programa de servidor a ser chamado. Em troca, ele recebe uma referência ao programa de servidor, podendo tratá-la como se ela fosse o próprio programa de servidor.

O modelo de objeto RDS incorpora essa funcionalidade com o objeto [RDS.DataSpace](dataspace-object-rds.md).

O programa de servidor é especificado com um identificador de programa, ou *ProgID*. O servidor usa o *ProgID* e o registro da máquina para localizar informações sobre o programa real a ser iniciado.

O RDS faz uma distinção interna, dependendo de o programa de servidor estar em um servidor remoto na Internet ou em uma intranet; em um servidor em uma rede local; ou em nenhum servidor, mas, em uma biblioteca de vínculo dinâmico local (DLL). Essa distinção determina como as informações são trocadas entre o cliente e o servidor e faz uma diferença real no tipo de referência retornado ao aplicativo cliente. Entretanto, do seu ponto de vista, essa distinção não possui significado especial; o que importa é que você receberá uma referência de programa que pode ser usada.

## <a name="rdsserverdatafactory"></a>RDSServer.DataFactory

O RDS fornece um programa de servidor padrão que pode executar uma consulta SQL na fonte de dados e retornar um objeto [Recordset](recordset-object-ado.md) ou usar um objeto **Recordset** e atualizar a fonte de dados.

O modelo de objeto RDS incorpora essa funcionalidade com o objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).

Além disso, esse objeto tem um método para criar um objeto **Recordset** vazio que você pode preencher programaticamente ([CreateRecordset](createrecordset-method-rds.md)) e outro método para converter um objeto **Recordset** em uma cadeia de caracteres de texto para criar uma página da Web ([ConvertToString](converttostring-method-rds.md)).

Com o ADO, você pode substituir parte do comportamento de comando e da conexão padrão de **RDSServer.DataFactory** com um manipulador **DataFactory** e um arquivo de personalização contendo parâmetros de conexão, comando e segurança.

O programa de servidor algumas vezes é chamado de *objeto corporativo*. Você pode criar o seu próprio objeto corporativo para executar um acesso a dados complicados, verificações de validade etc. Até mesmo ao escrever um objeto corporativo personalizado, você poderá criar uma instância de um objeto **RDSServer.DataFactory** e usar alguns de seus métodos para executar suas próprias tarefas.

## <a name="rdsdatacontrol"></a>RDS. DataControl

O RDS permite combinar a funcionalidade de **RDS.DataSpace** e **RDSServer.DataFactory**, e também permite que os controles visuais utilizem facilmente o objeto **Recordset** retornado por uma consulta de uma fonte de dados. Para o caso mais comum, o RDS tenta ao máximo obter acesso automaticamente às informações em um servidor e exibi-las em um controle visual.

O modelo de objeto RDS incorpora essa funcionalidade com o objeto [RDS.DataControl](datacontrol-object-rds.md).

O **RDS.DataControl** possui dois aspectos. Um deles refere-se à fonte de dados. Se você definir as informações de comando e de conexão usando as propriedades **Connect** e **SQL** de **RDS.DataControl**, elas utilizarão o **RDS.DataSpace** automaticamente para criar uma referência ao objeto **RDSServer.DataFactory** padrão. Em seguida, **RDSServer.DataFactory** utilizará o valor da propriedade **Connect** para se conectar à fonte de dados, utilizará o valor da propriedade **SQL** para obter um **Recordset** da fonte de dados e retornará o objeto **Recordset** a **RDS.DataControl**.

O segundo aspecto refere-se à exibição das informações retornadas de **Recordset** em um controle visual. Você pode associar um controle visual ao **RDS. DataControl** (em um processo chamado associação) e obter acesso às informações no objeto **Recordset** associado, exibindo resultados de consulta em uma página da Web no Microsoft Internet Explorer. Cada objeto **RDS.DataControl** acopla um objeto **Recordset**, que representa os resultados de uma única consulta, a um ou mais controles visuais (por exemplo, uma caixa de texto, uma caixa de combinação, um controle de grade etc.). É possível haver mais de um objeto **RDS.DataControl** em cada página. Cada objeto **RDS.DataControl** pode ser conectado a uma fonte de dados diferente e conter os resultados de uma consulta separada.

O objeto **RDS.DataControl** também possui seus próprios métodos de navegação, classificação e filtragem das linhas do objeto **Recordset** associado. Esses métodos são semelhantes, mas diferentes dos métodos no objeto ADO **Recordset**.

## <a name="events"></a>Eventos

O RDS oferece suporte a dois de seus próprios eventos, que são independentes do modelo de evento ADO. O [evento onReadyStateChange](onreadystatechange-event-rds.md) é chamado sempre que **o RDS. A propriedade DataControl** [ReadyState](readystate-property-rds.md) muda, notificando você quando uma operação assíncrona foi concluída, encerrada ou teve um erro com êxito. O evento [onError](onerror-event-rds.md) é chamado sempre que ocorre um erro, mesmo que ele ocorra durante uma operação assíncrona.

> [!NOTE]
> [!OBSERVAçãO] O Microsoft Internet Explorer oferece dois eventos adicionais aos do RDS  **onDataSetChanged** (o **Recordset** está funcional, mas ainda recupera linhas) e **onDataSetComplete** (o **Recordset** concluiu a recuperação de linhas).


