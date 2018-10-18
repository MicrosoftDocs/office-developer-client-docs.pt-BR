---
<<<<<<< Título cabeça: TOCTitle preparado Property (ADO): propriedade preparado (ADO) === título: preparado propriedade (ADO) TOCTitle: preparado propriedade (ADO)
>>>>>>> ms:assetid de mestre: 33becda2-faab-5000-8904-6ffd8c5805f2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15) ms:contentKeyID: ms.date 48544116: 18/09/2015 mtps_version: v=office.15 f1_keywords:
- ado210.chm1231161 f1_categories:
- Office.Version=v15
---

<<<<<<< Cabeça
# <a name="prepared-property-ado"></a>Propriedade Prepared (ADO)
=======
# <a name="prepared-property-ado"></a>Propriedade PREPARED (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica se uma versão compilada de um comando deve ser salva antes da execução.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **Boolean** que, se definido como **True**, indicará que o comando deve ser preparado.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Prepared** para que o provedor salve uma versão preparada (ou compilada) da consulta especificada na propriedade [CommandText](commandtext-property-ado.md) antes da primeira execução de um objeto [Command](command-object-ado.md). Isto pode fazer com que a primeira execução do comando demore, mas depois que o provedor compilar um comando, ele utilizará a versão compilada do comando para quaisquer execuções subsequentes, melhorando o desempenho.

Se a propriedade for **False**, o provedor executará o objeto **Command** diretamente sem criar uma versão compilada.

Se o provedor não oferecer suporte à preparação do comando, ele poderá retornar um erro assim que essa propriedade for definida como **True**. Se não retornar um erro, ele simplesmente ignorará a solicitação para preparar o comando e definirá a propriedade **Prepared** como **False**.

