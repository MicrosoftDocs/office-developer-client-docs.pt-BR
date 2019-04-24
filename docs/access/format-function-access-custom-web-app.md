---
title: Função Format (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Retorna um valor formatado de acordo com um padrão específico.
localization_priority: Priority
ms.openlocfilehash: 5331df30f276a7edd0571e9bf24c759d57ec6a54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308201"
---
# <a name="format-function-access-custom-web-app"></a>Função Format (aplicativo Web personalizado do Access)

Retorna um valor formatado de acordo com um padrão específico.
  
> [!NOTE]
> O recurso de armazenamento em nuvem descrito neste artigo não tem mais suporte no Office 2013 e Office 2016, e pode resultar no seguinte erro: > *Estamos com problemas de servidor, portanto, não podemos adicionar \<serviço\> agora. Tente novamente mais tarde.* > Para armazenamento em nuvem do Office Online, Office para iOS e Office para Android, você poderá pesquisar no nosso [Programa de Parceiros de Armazenamento de Nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Formato** (*Expressão*, *Formato*) 
  
A função **Formato** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Expressão*.  <br/> |Expressão de um tipo de dados com suporte para formatar.  <br/> |
| *Formato*  <br/> | Um padrão de formatação. O argumento de formato deve conter uma cadeia de caracteres de formato válida, como uma cadeia de caracteres de formato padrão (por exemplo, "C" ou "D") ou como um padrão de caracteres personalizados para datas e valores numéricos (por exemplo, "MMMM dd, (dddd) aaaa"). Para saber mais, consulte Comentários.  <br/> |
   
## <a name="remarks"></a>Comentários

Para o parâmetro *Formato*, você pode passar cadeias de caracteres que correspondam a qualquer um dos seguintes padrões: 
  
- [Cadeias de caracteres de formato numérico padrão](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [Cadeias de caracteres de formato numérico personalizado](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)
    
- [Cadeias de caracteres padrão de formato de data e hora](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)
    
- [Cadeias de caracteres de formato de data e hora](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)
    
Não é possível usar a função **Format** nas seguintes áreas de aplicativos Web do Access 2013: 
  
- Colunas calculadas ao nível da tabela
    
- Macros de interface do usuário
    
- Expressões nos modos de exibição (por exemplo, em formulários)
    

