// Tạo 3 nodes với tên "Lộc", "Thiên" và "Hưng"
CREATE (:Person {name: "Lộc"})
CREATE (:Person {name: "Thiên"})
CREATE (:Person {name: "Hưng"})

// Tạo quan hệ "cùng nhà" giữa "Hưng" và "Lộc"
MATCH (hung:Person {name: "Hưng"})
MATCH (loc:Person {name: "Lộc"})
CREATE (hung)-[:SAME_HOUSE]->(loc);

// Tạo quan hệ "đi học cùng" giữa "Thiên" và "Hưng"
MATCH (hung:Person {name: "Hưng"})
MATCH (thien:Person {name: "Thiên"})
CREATE (thien)-[:GOES_TO_SCHOOL_WITH]->(hung);

// Xem tất cả các node hiện có
MATCH (n) RETURN n

// Truy vấn tất cả các mối quan hệ của "Hưng"
MATCH (hung:Person {name: "Hưng"})-[r]-()
RETURN hung, r;


// Xóa mối quan hệ giữa "Hưng" và "Thiên"
MATCH (hien:Person {name: "Hưng"})-[r:GOES_TO_SCHOOL_WITH]->(thien:Person {name: "Thiên"})
DELETE r;

// Xóa node có tên "Thiên"
MATCH (thien:Person {name: "Thiên"})
DELETE thien;

