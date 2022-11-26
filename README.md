- 👋 Hi, I’m @sky9546
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
sky9546/sky9546 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
public class MainClass {
	
	static Map<String, List<String>> records = new Hashtable<>();

	public static void main(String[] args) {
		
		
		Map<String,String> hashTable = new HashMap<String,String>();
		hashTable.put("akash", "maths");
		
		Map<String,String> hashMap = new HashMap<String,String>();
		hashMap.put("akash", "history");
		hashMap.put("ak", "history");
		
		addRecord(hashTable);
		addRecord(hashMap);
		System.out.println(records);
		
		
	}
	
	static Map<String, List<String>> addRecord(Map<String, String> input) {
		for (Map.Entry<String, String> mapEntry : input.entrySet()) {
			List<String> record = records.get(mapEntry.getKey());
			if(record != null) {
				record.add(mapEntry.getValue());
			} else {
				record = new ArrayList<>();
				record.add(mapEntry.getValue());
			}
			records.put(mapEntry.getKey(), record);
		}
		return records;
	}

}
