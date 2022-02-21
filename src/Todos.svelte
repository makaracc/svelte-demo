<script>
  import TodoItem from "./TodoItem.svelte";
  import { db } from "./firebase";
  import {collectionData} from 'rxfire/firestore';
import {startWith} from 'rxjs/operators';

export let uid;
export let text = "some thing";
const query = db.collection("todos").where("uid", "==", uid);


const querySnapshot = await getDocs(collection(db, "users"));
querySnapshot.forEach((doc) => {
  console.log(`${doc.id} => ${doc.data()}`);
});
</script>