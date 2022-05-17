# Smart contract definition

### Giới thiệu <a href="#header-0" id="header-0"></a>

Hợp đồng thông minh được Nick Szabo mô tả lần đầu tiên vào những năm 1990. Vào thời điểm đó, ông định nghĩa hợp đồng thông minh là một công cụ để chính thức hóa và bảo mật mạng máy tính bằng cách kết hợp các giao thức với giao diện người dùng.

Szabo đã thảo luận về khả năng sử dụng hợp đồng thông minh trong nhiều lĩnh vực khác nhau có liên quan đến các thỏa thuận hợp đồng - chẳng hạn các hệ thống tín dụng, xử lý thanh toán và quản lý bản quyền nội dung.

Trong thế giới của tiền mã hóa, chúng ta có thể định nghĩa [hợp đồng thông minh](https://academy.binance.com/en/glossary/smart-contract) là một ứng dụng hoặc chương trình chạy trên blockchain. Hợp đồng thông minh giống như một hợp đồng kỹ thuật số bị bắt buộc thực hiện bởi một bộ quy tắc cụ thể. Các quy tắc này được code máy tính xác định trước, và tất cả các [node](https://academy.binance.com/vi/articles/what-are-nodes) trong mạng đều phải sao chép và thực thi các quy tắc đó.

Về bản chất, các hợp đồng thông minh trên blockchain cho phép tạo ra các giao thức không cần dựa trên sự tin cậy. Tức là hai bên trong hợp đồng có thể đưa ra các cam kết thông qua blockchain mà không cần phải biết hoặc tin tưởng lẫn nhau. Họ có thể đảm bảo rằng nếu các điều kiện của hợp đồng không được thỏa mãn, hợp đồng sẽ không được thực thi. Ngoài ra, việc sử dụng hợp đồng thông minh loại bỏ nhu cầu đối với các bên trung gian, giúp giảm đáng kể chi phí hoạt động.

Mặc dù giao thức Bitcoin đã hỗ trợ hợp đồng thông minh trong nhiều năm, nhưng chúng trở nên phổ biến bởi Vitalik Buterin, cha đẻ và nhà đồng sáng lập của [Ethereum](https://academy.binance.com/vi/articles/what-is-ethereum). Tuy nhiên, mỗi blockchain có một phương pháp triển khai hợp đồng thông minh khác nhau.&#x20;

Bài viết này sẽ tập trung vào các hợp đồng thông minh chạy trên Máy ảo Ethereum (Ethereum Virtual Machine, EVM), một phần thiết yếu của blockchain Ethereum.

\


### Hợp đồng thông minh hoạt động như thế nào? <a href="#header-1" id="header-1"></a>

Nói một cách đơn giản, hợp đồng thông minh hoạt động như một chương trình xác định. Nó thực thi một tác vụ cụ thể trong trường hợp thỏa mãn các điều kiện nhất định. Do đó, một hệ thống hợp đồng thông minh thường tuân theo các câu lệnh "nếu… thì…". Bất chấp tên gọi của nó, hợp đồng thông minh thựa ra không phải là một hợp đồng pháp lý và cũng không thông minh. Chúng chỉ là một đoạn code chạy trên một hệ thống phân tán (blockchain).

Trên mạng Ethereum, các hợp đồng thông minh chịu trách nhiệm thực thi và quản lý các hoạt động diễn ra trên blockchain khi những người dùng (địa chỉ) tương tác với nhau. Bất kỳ địa chỉ nào không phải là hợp đồng thông minh đều được gọi là tài khoản độc lập (viết tắt là EOA). Do đó, hợp đồng thông minh do máy tính kiểm soát và EOA do người dùng kiểm soát.

Về cơ bản, hợp đồng thông minh Ethereum bao gồm một hợp đồng code và hai khóa công khai. Khóa công khai thứ nhất là khóa do người tạo hợp đồng cung cấp. Khóa còn lại đại diện cho chính hợp đồng, khóa này có vai trò như một mã định danh kỹ thuật số duy nhất cho mỗi hợp đồng thông minh.

Hợp đồng thông minh được triển khai thông qua giao dịch trên blockchain và chúng chỉ được kích hoạt khi một EOA (hoặc các hợp đồng thông minh khác) gọi chúng. Tuy nhiên, kích hoạt đầu tiên luôn từ phía EOA (người dùng).

\


### Các tính năng chính khác <a href="#header-2" id="header-2"></a>

Hợp đồng thông minh Ethereum thường trình có các đặc điểm sau:

Phân tán. Hợp đồng thông minh được sao chép và phân phối trong tất cả các node của mạng Ethereum. Đây là một điểm khác biệt so với các giải pháp khác dựa trên các máy chủ tập trung.

Tính xác định. Hợp đồng thông minh chỉ thực hiện các hành động mà chúng được thiết kế để thực hiện trong trường hợp các điều kiện được thỏa mãn. Bên cạnh đó, các kết quả của hợp đồng thông minh không đổi, dù người thực hiện là ai.

Tự động. Hợp đồng thông minh có thể tự động hóa tất cả các loại tác vụ, nó hoạt động như một chương trình tự thực hiện. Tuy nhiên, trong hầu hết các trường hợp, nếu hợp đồng thông minh không được kích hoạt, nó sẽ duy trì trạng thái "không hoạt động" và sẽ không thực hiện bất kỳ hành động nào.

Không thể sửa đổi. Không thể sửa đổi hợp đồng thông minh sau khi triển khai. Chỉ có thể "xóa" chúng nếu chức năng này đã được thêm vào từ trước. Do đó, có thể nói rằng hợp đồng thông minh có thể cung cấp code chống giả mạo.

Có thể tùy chỉnh. Trước khi triển khai, hợp đồng thông minh có thể được mã hóa theo nhiều cách khác nhau. Vì vậy, chúng có thể được sử dụng để tạo ra nhiều loại ứng dụng phi tập trung ([Dapp](https://academy.binance.com/en/glossary/decentralized-application)). Điều này là bởi Ethereum là một blockchain [Turing hoàn chỉnh](https://academy.binance.com/en/glossary/turing-complete).

Không cần dựa trên sự tin cậy. Hai hoặc nhiều bên của hợp đồng có thể tương tác thông qua hợp đồng thông minh mà không cần biết hoặc tin tưởng lẫn nhau. Ngoài ra, công nghệ blockchain đảm bảo tính chính xác của dữ liệu.

Tính minh bạch. Vì các hợp đồng thông minh hoạt động trên một blockchain công khai, không ai có thể thay đổi mã nguồn của chúng, mặc dù bất kỳ ai cũng có thể xem được.

\


#### Tôi có thể thay đổi hoặc xóa hợp đồng thông minh không?

Không thể thêm các chức năng mới vào hợp đồng thông minh Ethereum sau khi triển khai. Tuy nhiên, nếu người tạo ra hợp đồng đưa vào một chức năng gọi là TỰ HỦY (SELFDESTRUCT) trong code, họ có thể "xóa" hợp đồng thông minh trong tương lai - và thay thế nó bằng một hợp đồng mới. Ngược lại, nếu chức năng này không được đưa vào code từ trước, họ sẽ không thể xóa hợp đồng thông minh đó.

Hãy lưu ý đến các hợp đồng thông minh có khả năng nâng cấp - với loại hợp đồng này, các nhà phát triển có thể thay đổi hợp đồng thông minh ở một mức độ nào đó. Có nhiều cách để tạo các hợp đồng thông minh có khả năng nâng cấp với mức độ phức tạp khác nhau.

Lấy một ví dụ đơn giản, hãy tưởng tượng rằng một hợp đồng thông minh được chia thành nhiều hợp đồng nhỏ hơn. Một số hợp đồng nhỏ này không thể thay đổi còn một số khác có chức năng 'xóa'. Điều này nghĩa là, có thể xóa và thay thế một phần của bộ mã (hợp đồng thông minh), trong khi các chức năng khác không thay đổi.

\


### Ưu điểm và trường hợp sử dụng <a href="#header-3" id="header-3"></a>

Với bản chất là một bộ code có thể lập trình, hợp đồng thông minh có khả năng tùy chỉnh cao và có thể được thiết kế theo nhiều cách khác nhau để có thể cung cấp nhiều loại dịch vụ và giải pháp.

Là các chương trình phi tập trung và tự thực hiện, hợp đồng thông minh giúp tăng tính minh bạch và giảm chi phí hoạt động. Nếu được triển khai đúng cách, chúng cũng có thể tăng hiệu quả vận hành và giảm chi phí hành chính.

Hợp đồng thông minh đặc biệt hữu ích trong các tình huống liên quan đến việc chuyển hoặc trao đổi tiền giữa hai hoặc nhiều bên.

Nói cách khác, có thể thiết kế hợp đồng thông minh cho nhiều [trường hợp sử dụng.](https://academy.binance.com/vi/articles/blockchain-use-cases) Một số ví dụ bao gồm việc tạo ra các tài sản được token hóa, hệ thống bầu chọn, ví tiền mã hóa, các sàn giao dịch phi tập trung, trò chơi và ứng dụng di động. Ngoài ra, cũng có thể kết hợp hợp đồng thông minh với các giải pháp blockchain khác để giải quyết các vấn trong các lĩnh vực [chăm sóc sức khỏe](https://academy.binance.com/vi/articles/blockchain-use-cases-healthcare), [từ thiện](https://academy.binance.com/vi/articles/blockchain-use-cases-charity), [chuỗi cung ứng](https://academy.binance.com/vi/articles/blockchain-use-cases-supply-chain), [quản trị](https://academy.binance.com/vi/articles/blockchain-use-cases-governance), và [tài chính phi tập trung (DeFi)](https://academy.binance.com/en/glossary/defi).

\


#### ERC-20

Các token được phát hành trên blockchain Ethereum tuân theo một tiêu chuẩn được gọi là [ERC-20](https://academy.binance.com/en/glossary/erc-20). Tiêu chuẩn này mô tả các chức năng cốt lõi của tất cả các token được tạo ra trên Ethereum. Do đó, các tài sản kỹ thuật số này thường được gọi là các token ERC-20 và phần lớn các loại tiền mã hóa hiện nay sử dụng tiêu chuẩn này.Nhiều công ty blockchain và công ty khởi nghiệp đã triển khai các hợp đồng thông minh để phát hành các token kỹ thuật số của họ trên mạng Ethereum. Sau khi phát hành, phần lớn các công ty này đã phân phối các token ERC-20 của họ thông qua các sự kiện [Phát hành tiền mã hóa lần đầu (ICO)](https://academy.binance.com/vi/articles/what-is-an-ico). Việc sử dụng hợp đồng thông minh chủ yếu giúp trao đổi tiền và phân phối token theo cách thức không cần dựa trên sự tin cậy và hiệu quả.

\


### Các hạn chế <a href="#header-4" id="header-4"></a>

Hợp đồng thông minh được tạo ra bởi các dòng code máy tính do con người viết ra. Điều này mang lại nhiều rủi ro vì code có khả năng bị tấn công và có lỗi. Tốt nhất, chúng nên được viết và triển khai bởi các lập trình viên giàu kinh nghiệm, đặc biệt là khi có liên quan đến thông tin nhạy cảm hoặc số tiền lớn.

Ngoài ra, có một số ý kiến cho rằng các hệ thống tập trung cũng có thể cung cấp hầu hết các giải pháp và chức năng mà hợp đồng thông minh mang lại. Tuy nhiên, điều khác biệt là ở chỗ, các hợp đồng thông minh chạy trên một mạng ngang hàng (P2P) phân tán thay vì trên một máy chủ tập trung. Đồng thời các hợp đồng thông minh dựa trên hệ thống blockchain nên rất khó hoặc không thể sửa đổi và can thiệp.

Tính chất không thể thay đổi là một ưu điểm lớn, tuy nhiên trong một số trường hợp có thể là nhược điểm. Ví dụ, khi một Tổ chức Tự trị Phi tập trung (DAO) có tên là "The DAO" bị hack vào năm 2016, hàng triệu ether (ETH) đã bị đánh cắp do có sai sót trong code hợp đồng thông minh của họ.

Vì hợp đồng thông minh của họ là không thể thay đổi, nên các nhà phát triển không thể sửa code. Điều này cuối cùng đã dẫn đến một [hard fork](https://academy.binance.com/vi/articles/hard-forks-and-soft-forks), tạo ra chuỗi Ethereum thứ hai. Nói một cách đơn giản, một chuỗi "đã hoàn nguyên" vụ tấn công và trả lại tiền cho các chủ sở hữu hợp pháp (chuỗi này là một phần của blockchain Ethereum hiện tại). Chuỗi còn lại đã quyết định không can thiệp vào vụ tấn công vì cho rằng không được thay đổi những điều xảy ra trên blockchain (chuỗi này hiện được gọi là Ethereum Classic).

Điều quan trọng cần lưu ý là vấn đề không đến từ blockchain Ethereum. Thay vào đó, là lỗi trong việc thực hiện hợp đồng thông minh.

Hợp đồng thông minh còn có một hạn chế khác liên quan đến tình trạng pháp lý của chúng. Điều này không chỉ bởi vì các hợp đồng thông minh có một trạng thái pháp lý không rõ ràng, mà còn bởi vì các hợp đồng thông minh không phù hợp với khung pháp lý hiện tại.

Ví dụ, nhiều hợp đồng yêu cầu cả hai bên phải có danh tính rõ ràng và trên 18 tuổi. Tính chất ẩn danh của người dùng cùng với việc không sử dụng các bên trung gian của công nghệ blockchain có thể khiến nó không đáp ứng được những yêu cầu này. Mặc dù có thể có giải pháp cho vấn đề này, nhưng việc có thể áp dụng các biện pháp bắt buộc về mặt pháp lý cho hợp đồng thông minh là một thách thức thực sự - đặc biệt khi thực hiện trên các các mạng phân tán, không biên giới.

\


### Các ý kiến chỉ trích <a href="#header-5" id="header-5"></a>

Một số người yêu thích blockchain kỳ vọng hợp đồng thông minh là giải pháp sẽ sớm thay thế và tự động hóa một hầu hết các hoạt động thương mại và hệ thống hành chính của chúng ta. Mặc dù điều này có thể trở thành hiện thực, hợp đồng khó có thể trở thành chuẩn mực.

Hợp đồng thông minh chắc chắn một sản phẩm công nghệ thú vị. Tuy nhiên, tính chất phân tán, xác định, minh bạch và không thể thay đổi có thể khiến chúng khó sử dụng trong một số tình huống.

Về cơ bản, các ý kiến phê bình xem hợp đồng thông minh không phải là giải pháp phù hợp cho nhiều vấn đề trong thế giới thực. Trên thực tế, một số tổ chức nhận thấy các giải pháp dựa trên máy chủ thông thường có nhiều ưu điểm hơn.&#x20;

So với các hợp đồng thông minh, việc bảo trì các máy chủ tập trung dễ hơn và có chi phí thấp hơn, đồng thời dường như có tốc độ hoạt động nhanh hơn cũng như khả năng liên lạc qua mạng (khả năng tương tác) hiệu quả hơn.

\


### Tổng kết <a href="#header-6" id="header-6"></a>

Có thể khẳng định rằng hợp đồng thông minh đã có ảnh hưởng lớn đến thế giới tiền mã hóa, và chúng chắc chắn đã làm thay đổi không gian blockchain. Mặc dù người dùng cuối có thể không tương tác trực tiếp với các hợp đồng thông minh, nhưng những hợp đồng này có thể là cơ sở cho hàng loạt các ứng dụng trong tương lai, từ dịch vụ tài chính đến quản lý chuỗi cung ứng.

Khi kết hợp với nhau, hợp đồng thông minh và blockchain có khả năng thay đổi hầu hết các lĩnh vực trong xã hội của chúng ta. Nhưng chúng ta cần chờ đợi để xem liệu những công nghệ đột phá này có thể vượt qua nhiều rào cản để được áp dụng trên quy mô lớn hay không.
