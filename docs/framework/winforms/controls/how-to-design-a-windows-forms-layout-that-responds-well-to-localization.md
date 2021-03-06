---
title: '方法 : ローカリゼーションに対応した Windows フォーム レイアウトをデザインする'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- application design [Windows Forms], localization
- Windows Forms, localization
- localization [Windows Forms], Windows Forms layout
ms.assetid: d13eff2d-701c-4b6e-8838-3885cbfb7223
ms.openlocfilehash: c72cae58e8486f1187fd27d200522a43dca328ca
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44086675"
---
# <a name="how-to-design-a-windows-forms-layout-that-responds-well-to-localization"></a>方法 : ローカリゼーションに対応した Windows フォーム レイアウトをデザインする
ローカライズが可能なフォームを作成すると、各国市場向けの開発期間が大幅に短縮されます。 <xref:System.Windows.Forms.TableLayoutPanel> コントロールを使用すると、<xref:System.Windows.Forms.Control.Text%2A> プロパティ値の変更によってコントロールのサイズが変更された際に、これに適切に応答するレイアウトを実装できます  
  
## <a name="example"></a>例  
 このフォームでは、表示される文字列値を他の言語に翻訳するときに、均等に調整されるレイアウトを作成する方法を示します。 この翻訳プロセスのことを "*ローカリゼーション*" といいます。 詳細については、「[ローカリゼーション](../../../../docs/standard/globalization-localization/localization.md)」を参照してください。  
  
 Visual Studio では、このタスクに対する広範なサポートが用意されています。  「[チュートリアル: ローカライズの際に均等に調整されるレイアウトの作成](https://msdn.microsoft.com/library/7k9fa71y\(v=vs.110\))」も参照してください。  
  
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/CS/localizableform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.LocalizableForm#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.LocalizableForm/VB/localizableform.vb#1)]  
  
1.  [方法: TableLayoutPanel コントロール内でコントロールを配置して伸縮する](how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control.md)  
  
2.  [チュートリアル: FlowLayoutPanel を使用した Windows フォーム上のコントロールの配置](https://msdn.microsoft.com/library/z9w7ek2f\(v=vs.110\))  
  
3.  [方法: TableLayoutPanel コントロールの行と列を拡大する](how-to-span-rows-and-columns-in-a-tablelayoutpanel-control.md)  
  
4.  [方法: TableLayoutPanel コントロールの列と行を編集する](how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control.md)  
  
5.  [チュートリアル: Windows フォーム コントロールのスマート タグを使用した共通タスクの実行](https://msdn.microsoft.com/library/xhz359sc\(v=vs.110\))  
  
6.  [チュートリアル: TableLayoutPanel を使用した Windows フォーム上のコントロールの配置](https://msdn.microsoft.com/library/w4yc3e8c\(v=vs.110\))  
  
7.  [チュートリアル: Padding、Margin、および AutoSize プロパティを使用した Windows フォーム コントロールのレイアウト](https://msdn.microsoft.com/library/3z3f9e8b\(v=vs.110\))  
  
8.  [方法: AutoSize と TableLayoutPanel コントロールを使用して Windows フォームのローカリゼーションをサポートする](https://msdn.microsoft.com/library/1zkt8b33\(v=vs.110\))  
  
9. [チュートリアル: データ入力用のサイズ変更可能な Windows フォームの作成](https://msdn.microsoft.com/library/991eahec\(v=vs.110\))  
  
## <a name="compiling-the-code"></a>コードのコンパイル  
 この例で必要な要素は次のとおりです。  
  
-   System、System.Data、System.Drawing、および System.Windows.Forms の各アセンブリへの参照。  
  
 コマンドラインからこの例を Visual Basic または Visual c# の構築方法の詳細については、次を参照してください。 [、コマンドラインからビルドする](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md)または[コマンド ライン ビルドで csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)します。 新しいプロジェクトにコードを貼り付けることによって、この例では、Visual Studio を構築することもできます。  「[方法: 完成した Windows フォーム コードの例を Visual Studio を使ってコンパイルして実行する](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\))」も参照してください。  
  
## <a name="see-also"></a>関連項目  
 <xref:System.Windows.Forms.TableLayoutPanel>  
 <xref:System.Windows.Forms.FlowLayoutPanel>  
 [ローカリゼーション](../../../../docs/standard/globalization-localization/localization.md)
