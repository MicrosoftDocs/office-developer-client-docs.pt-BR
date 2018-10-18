---
<<<<<<< Título cabeça: TOCTitle de propriedade de Item (ADO): propriedade de Item (ADO) === título: propriedade (ADO) Item TOCTitle: Item propriedade (ADO)
>>>>>>> ms:assetid de mestre: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: ms.date 48545767: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="item-property-ado"></a>Propriedade Item (ADO)
=======
# <a name="item-property-ado"></a>Propriedade item (ADO)
>>>>>>> mestre

**Aplica-se a**: Access 2013 | Office 2013

Indica um membro específico de uma coleção, por nome ou número ordinal.

## <a name="syntax"></a>Sintaxe

Definir o*objeto* = *conjunto*. Item (Index)

<<<<<<< Cabeça
## <a name="return-value"></a>Valor retornado
=======
## <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

Retorna uma referência de objeto.

## <a name="parameters"></a>Parâmetros

- *Index*

- Uma expressão **Variant** avaliada para o nome ou para o número ordinal de um objeto em uma coleção.

## <a name="remarks"></a>Comentários

Use a propriedade **Item** para retornar um objeto específico em uma coleção. Se o **Item** não puder encontrar um objeto da coleção correspondente ao argumento de *índice* , ocorrerá um erro. Além disso, algumas coleções não oferecem suporte a objetos nomeados; para essas coleções, use referências de números ordinais.

A propriedade **Item** é a propriedade padrão para todas as coleções; assim, os formulários de sintaxe a seguir são intercambiáveis:

```vb
    collection.Item (Index)
    collection (Index)
```
